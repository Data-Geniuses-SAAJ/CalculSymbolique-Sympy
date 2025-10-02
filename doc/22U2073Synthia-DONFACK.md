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

## 📅 Mise à jour du 02 Octobre 2025 : Entropie Croisée Binaire (BCE)

L'étude de la fonction de Perte d'**Entropie Croisée Binaire** (Binary Cross-Entropy ou Log Loss) a été complétée, combinant l'approche symbolique (SymPy) et l'application pratique (NumPy/Matplotlib).

### 🎯 Objectifs Couverts (Exercice 1, BCE)

| Objectif | Réalisé | Détails |
| :--- | :--- | :--- |
| **Gradient** | ✅ | [cite_start]Expression analytique du gradient fournie[cite: 5]. |
| **Convexité** | ✅ | [cite_start]Propriété de stricte convexité démontrée via la Hessienne[cite: 6]. |
| **Courbes** | ✅ | [cite_start]Représentation de la surface de perte 3D et des courbes de niveau ("ellipses") sur le dataset Iris[cite: 9]. |
| **Tangente** | ✅ | [cite_start]Équation de la tangente à la courbe de niveau trouvée au point $P(0.8, -0.3)$[cite: 10]. |

### 🔍 Synthèse des Résultats Clés
* **Gradient ($\partial L / \partial \hat{y}$)** : $\frac{\hat{y} - y}{\hat{y}(1 - \hat{y})}$
* **Convexité** : **Strictement Convexe**, car la Hessienne ($\frac{\partial^2 L}{\partial \hat{y}^2}$) est strictement positive.

---
## 🚧 Autres Fonctions de Perte (Planification)
* Erreur Quadratique Moyenne (MSE)
* Entropie Croisée Catégorielle
* Perte de Huber

