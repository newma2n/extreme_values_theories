# 📈 Extreme Values & Copulas — Notebooks

Ce dépôt regroupe une série de notebooks Python conçus pour explorer les fondements théoriques et pratiques de la **théorie des valeurs extrêmes** (EVT) et des **copules**. Il s'agit d'un travail de consolidation réalisé en préparation d’un projet doctoral sur l’inférence pour données extrêmes dépendantes (Thèses Tandem Inria 2025-2026).

---

## 🧠 Objectifs du projet

- Comprendre et mettre en œuvre les **lois de valeurs extrêmes** : GEV (Generalized Extreme Value), GPD (Generalized Pareto).
- Étudier l’impact de la **dépendance temporelle** dans l’analyse d’événements rares (ex : rendements extrêmes).
- Explorer les **copules** comme outil de modélisation de la dépendance non linéaire (au-delà des corrélations classiques).
- Réaliser des **inférences fréquentistes et bayésiennes** dans des contextes de dépendance forte.
- Appliquer ces méthodes à des **données financières réelles** (log-rendements du S&P 500).

---

## 🧪 Contenu du dépôt

| Notebook | Description |
|----------|-------------|
| `GEV.ipynb` | Modélisation des maxima annuels de hauteur de mer (Port Pirie) via la loi GEV. |
| `EVT_AD.ipynb` | Détection d’anomalies extrêmes dans des séries temporelles via EVT. |
| `Inférence fréquentiste & bayésienne des rendements extrêmes dépendants.ipynb` | Inférence mixte sur les rendements extrêmes du S&P 500, incluant copules empiriques. |
| `intro_copules.ipynb` | Introduction aux copules, définition, propriétés fondamentales et visualisation. |
| `simulation_copules.ipynb` | Simulation de données dépendantes via différentes familles de copules. |
| `fitting_data_copula.ipynb` | Ajustement de copules à des données réelles, estimation paramétrique. |
| `Estimation bayésienne par copule.ipynb` | Inférence bayésienne des paramètres de dépendance par copule (MCMC, prior/postérieur). |

---

## 📘 Prérequis

- Python ≥ 3.8
- Librairies : `numpy`, `scipy`, `matplotlib`, `seaborn`, `statsmodels`, `copulas`, `pymc`, `arviz`, `pandas`

Tu peux installer les dépendances avec :

```bash
pip install -r requirements.txt
```

---

## 💼 Utilisation

Tu peux ouvrir chaque notebook indépendamment pour explorer les visualisations, les calculs et les analyses. Chaque notebook est **autonome**, avec explications, équations, graphiques, simulations et inférences intégrés.

Pour lancer :

```bash
jupyter notebook
```

---

## 📎 Liens utiles

- 🎓 Certificat associé : [Certificate of Completion — Practical Anomaly Detection (appliedAI Institute)](https://github.com/newma2n/extreme_values_theories/blob/main/Certificate_of_Completion.pdf)
- 🔗 Profil GitHub : [https://github.com/newma2n](https://github.com/newma2n)
- 📑 CV et projets : disponibles sur demande

---

## 🧭 À propos

Ce dépôt est maintenu par **Hamidou Kane** dans le cadre de la préparation d’une **candidature doctorale en inférence extrême**. Il est pensé comme une base rigoureuse, évolutive et pédagogique pour les futurs travaux de recherche.

---