# Présentation : Calcul Symbolique et utilisation de SymPy

Ce dépôt contient une présentation **LaTeX Beamer** sur le **calcul symbolique** et l'utilisation de la bibliothèque **SymPy** en Python.

## 📌 Contenu

* Introduction au calcul symbolique
* Présentation de SymPy (bibliothèque Python de calcul formel)
* Manipulation d'expressions symboliques
* Calculs avancés (dérivées, intégrales, équations, limites, matrices)
* Exemples pratiques d'utilisation
* Applications en éducation, recherche, physique et ingénierie

## 📂 Arborescence du dépôt

* `Présentation.pdf` → Version PDF compilée de la présentation
* `Operations_de_base_Sympy.ipynb` → Notebook Jupyter illustrant l’importation de SymPy et les opérations de base (symboles, expressions, dérivées, intégrales, équations, matrices)
* `doc/` → Dossier contenant les fichiers `.md` de participation et contributions de chaque membre
* `README.md` → Ce fichier de description du projet
* `TPE1/` → Dossier contenant la présentation pdf et le notebook du TPE n1


## 📦 Installation de SymPy

Avant d’exécuter le notebook ou les exemples de code, installez SymPy :

```bash
pip install sympy
```

## 🚀 Exemples de code

### Déclaration de symboles

```python
from sympy import symbols, init_printing
init_printing(use_unicode=True)
x, y = symbols('x y')
```

### Manipulation d'expressions

```python
expr = x + 2*y
expanded_expr = expand(x*expr)  # x**2 + 2*x*y
```

### Calculs avancés

```python
from sympy import diff, integrate, limit, solve, Matrix, sin, exp

# Dérivée
derivee = diff(sin(x)*exp(x), x)

# Résolution d’équation
solution = solve(x**2 - 3*x - 2, x)
```

## 👨‍🏫 Applications

* Éducation : apprentissage des mathématiques symboliques
* Recherche : modélisation et calcul formel
* Sciences appliquées : physique, ingénierie, optimisation

---

✍️ Présentation réalisée en **LaTeX Beamer** avec exemples pratiques en **Python / SymPy**, accompagnée d’un **notebook interactif** et d’une documentation collaborative dans `doc/`.
