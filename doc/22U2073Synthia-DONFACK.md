# INF4127: Optimisation II - Travaux Pratiques
# Cahier de suivi de projet – Membre

## 1. Informations générales

- **Nom et prénom :** DONFACK Synthia Calorine
- **Rôle dans le projet :** Concepteur de la présentation, responsable de la conception et de l'intégration des slides en LaTeX, en m'inspirant des recherches fournies par l'équipe.
- **Période de participation :** 30 septembre 2025 - 1er octobre 2025

## 2. Suivi hebdomadaire / par séance

| Date | Tâches prévues | Tâches réalisées | Difficultés rencontrées | Solutions / Prochaines étapes |
|------|----------------|------------------|-------------------------|-------------------------------|
| 30/09/2025 | Recherches individuelles sur les concepts de calcul symbolique et SymPy ; collecte des contributions de l'équipe. | Recherche sur les bases du calcul symbolique (définition, principes, analogies) ; intégration des idées de l'équipe pour les slides d'introduction et d'applications. | Coordination des recherches individuelles dispersées ; besoin d'harmoniser les styles. | Synthétiser les contributions ; préparer la structure LaTeX. Prochaine étape : Finaliser les slides techniques. |
| 01/10/2025 | Synthèse du rapport général et conception de la présentation (slides sur définition, analogies, outils, exemples). | Synthèse complète du rapport ; création des slides en LaTeX (titre, question simple, problème concret, définition, analogie, pourquoi, applications, outils, SymPy, philosophie, installation, exemples guidés). | Problèmes d'affichage des codes Python dans les slides dus à l'encodage des accents. | Correction de la configuration listings en LaTeX ; test de compilation. Prochaine étape : Validation finale et présentation. |

## 3. Contributions techniques

### Fichiers modifiés ou créés :
- `Presentation.pdf` (synthèse du rapport général, incluant les sections inspirées des recherches de l'équipe)
- `presentation.tex` (fichier LaTeX de la présentation : conception des slides, intégration des exemples et analogies)
- `22U2073Synthia-DONFACK.md` (ce fichier de suivi personnel)

### Fonctionnalités ou ajouts spécifiques :
- Conception visuelle des slides (utilisation du thème Madrid/seahorse, blocs, colonnes, tikz pour workflow)
- Intégration d'exemples inspirés des recherches de l'équipe (e.g., racine carrée de 8, résolution d'équations, analogie architecte/constructeur)
- Synthèse des sections générales (définition, pourquoi, applications) et techniques (outils, SymPy, exemples guidés)

## 4. Réflexion personnelle

### Compétences acquises :
- Maîtrise de LaTeX pour les présentations Beamer (gestion des thèmes, listings pour codes, tikz pour diagrammes)
- Synthèse de recherches collectives en un document cohérent et visuellement attractif
- Compréhension approfondie du calcul symbolique et de SymPy via l'intégration pratique dans les slides

### Améliorations possibles :
- Ajouter des animations ou des transitions dans les slides pour plus d'interactivité
- maitrise approfondie de sympy

## 5. Validation

- **Signature / Nom de l'étudiant :** DONFACK Synthia Calorine
- **Date de validation :** 02/10/2025
---


.

# 🎓 INF4127: Optimisation II - Travaux Pratiques n°1 (TPE n°1)

Ce dépôt contient le travail pratique (TPE n°1) du cours d'Optimisation II, concernant l'analyse des propriétés fondamentales de différentes fonctions de perte.

[cite_start]Le travail, initialement l'Exercice 1 de la Fiche de TPE n°1[cite: 3], a été divisé entre les étudiants pour optimiser le temps de réalisation (contrainte fixée à moins de 10 heures). Mon rôle était de prendre en charge l'analyse complète de la fonction de **Perte d'Entropie Croisée Binaire (BCE)**.

Le code d'analyse complet se trouve dans le notebook `TP_INF4127_BCE.ipynb`.

---

## I. Analyse de l'Entropie Croisée Binaire (BCE)

L'Entropie Croisée Binaire (Binary Cross-Entropy ou Log Loss) est la fonction de perte standard pour les problèmes de classification binaire.

### 1. Expressions du Gradient (Question 1)

[cite_start]Utilisation du calcul symbolique (`sympy`) pour déterminer l'expression du gradient $\nabla L$ par rapport à la prédiction $\hat{y}$. [cite: 5]

La fonction de perte pour une observation est :
$$
L(y, \hat{y}) = -[y \log(\hat{y}) + (1-y) \log(1-\hat{y})]
$$

L'expression du gradient est :
$$
\frac{\partial L}{\partial \hat{y}} = \frac{\hat{y} - y}{\hat{y}(1 - \hat{y})}
$$

### 2. Étude de la Convexité (Question 2)

[cite_start]L'étude de la convexité repose sur le calcul de la dérivée seconde (la Hessienne) par rapport à $\hat{y}$. [cite: 6]

L'expression de la Hessienne est :
$$
\frac{\partial^2 L}{\partial \hat{y}^2} = \frac{y}{\hat{y}^2} + \frac{1 - y}{(1 - \hat{y})^2}
$$

**Conclusion :** Puisque $\hat{y} \in (0, 1)$ et $y \in \{0, 1\}$, le terme $\frac{\partial^2 L}{\partial \hat{y}^2}$ est **strictement positif** ($\gt 0$). La fonction de perte BCE est donc **Strictement Convexe**, ce qui garantit l'existence d'un unique minimum global lors de l'optimisation.

### 3. Application Pratique et Visualisations (Question 3a)

[cite_start]Un jeu de données de classification binaire, le dataset **Iris (Classes 0 et 1)**[cite: 7], a été utilisé pour modéliser une fonction de perte $L(w_1, w_2)$ basée sur un modèle de Régression Logistique.

[cite_start]Les visualisations (Courbes 3D et Courbes de Niveau) ont confirmé l'aspect convexe de la surface de perte dans l'espace des paramètres $(\mathbf{w})$. [cite: 9]

### 4. Équation de la Tangente à l'Ellipse (Question 3b)

[cite_start]L'équation de la tangente à la courbe de niveau (l'ellipse) au point $P(w_1^P, w_2^P) = (0.8, -0.3)$ a été calculée en utilisant la propriété que la tangente est perpendiculaire au vecteur gradient $\nabla L(P)$. [cite: 10]

Le vecteur gradient au point $P$ est calculé numériquement : $\nabla L(P) = (g_1, g_2)$.

L'équation de la tangente est donnée par :
$$
g_1 \cdot (w_1 - w_1^P) + g_2 \cdot (w_2 - w_2^P) = 0
$$

Le notebook inclut le calcul exact des valeurs $g_1$ et $g_2$ et l'équation finale sous forme $w_2 = a \cdot w_1 + b$, ainsi que la visualisation graphique de cette tangente.
