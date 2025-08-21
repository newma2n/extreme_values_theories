# 📈 Extreme Value Theories & Copulas — Autodidact Research Projects

Ce dépôt regroupe une série de projets explorant les **théories des valeurs extrêmes (EVT)** et la **modélisation de dépendance via copules**, appliquées à des données environnementales et financières.  
Les notebooks sont le fruit d’un **travail de recherche personnel et autodidacte**, intégrant à la fois des fondements théoriques et des implémentations pratiques en Python.

---

## 🧭 Table des projets

### 1. `EVT_AD.ipynb` — Détection d’anomalies par EVT sur données Taxi NYC

* Objectif : détecter des anomalies rares dans les appels de taxi à NYC (agrégés par pas de 30 min).
* Ajustement d'une loi GEV sur la queue de distribution (méthode du maximum de vraisemblance).
* Estimation de quantiles extrêmes et seuils d’alerte.
* Extraction de journées inhabituelles comme le 10 janvier 2015 (lendemain des attentats Charlie Hebdo).
* Utilisation de `scipy.stats.genextreme`, QQ-plot, histograms, etc.

---

### 2. `univariatetimeseries.ipynb` — Prévision univariée et dépendance extrême via copules

* Données : températures maximales journalières à China Lake (États-Unis). Construction des paires temporelles \((X_t, X_{t+1})\) puis transformation en pseudo-observations par rangs.
* Ajustement de copules **gaussienne**, **Clayton**, **Gumbel** et **Frank** ; paramètres obtenus par inversion du tau de Kendall.
* Évaluation de la qualité d’ajustement par la statistique de **Cramér–von Mises** sur les pseudo-observations, avec comparaison visuelle; sélection du modèle minimisant cette statistique.
* Simulation **conditionnelle** (distribution de l’observation suivante sachant l’observation courante) afin d’analyser la **co-extrémalité temporelle** ;
* Résultat :un modèle probabiliste intégrant explicitement la dépendance extrême.


---

### 3. `GEV.ipynb` — Maxima annuels des hauteurs marines à Port Pirie

* Données issues du livre `coles2001gev` : hauteurs annuelles maximales de la mer.
* Ajustement d’une loi GEV par maximum de vraisemblance.
* Analyse des trois cas (Fréchet, Gumbel, Weibull) selon le paramètre ξ.
* Validation visuelle (PP-plot, QQ-plot).
* Estimation de niveaux de retour pour matriser les risques.

---

### 4. `Inférence fréquentiste & bayésienne des rendements extrêmes dépendants.ipynb`-Inférence des rendements extrêmes avec d´ependance (S&P 500) 

* Étude des extrêmes sur les log-rendements journaliers du S&P 500 (1990–2025).
* Ajustement d’une GEV sur blocs de maxima (fréquentiste).
* Étude de la dépendance temporelle via copules empiriques.
* Estimation bayésienne des paramètres GEV (avec visualisation de la posterior).
* Comparaison des approches fréquentiste vs bayésienne sur l'estimation des quantiles extrêmes.

---

### 5. `Estimation bayésienne par copule.ipynb`

* Présentation pédagogique du **concept de copule** pour modéliser des lois jointes corrélées.
* Implémentation de **copules paramétriques** (Gaussienne, Clayton, Gumbel, Student-t) sur des données synthétiques.
* Méthode **bayésienne** pour estimer les paramètres de dépendance (via MCMC et prior uniforme).
* Illustration du **processus de transformation** entre espace gaussien multivarié et espace d'observation.
* Simulation de **scénarios extrêmes**, visualisation des **surfaces de densité conjointe**.
* **Objectif :** modéliser la dépendance structurelle entre variables, même lorsque les marges ne sont pas normales.


---

### 6. `fitting_data_copula.ipynb`

* Ajustement de **copules paramétriques** (Clayton, Gumbel, Frank, Gaussienne) à des données synthétiques ou réelles.
* Estimation des **paramètres de dépendance** par vraisemblance (méthode canonique).
* Comparaison de la qualité d’ajustement via les **niveaux de dépendance dans les queues** (Kendall’s τ).
* Visualisation de la **dépendance jointe** et des **régions extrêmes** dans l’espace copule.
* **Objectif :** identifier la structure de dépendance extrême entre deux variables, au-delà des corrélations linéaires.


---
### 7. `intro_copules.ipynb`

* Présentation pédagogique des **fondements théoriques des copules** : fonction de répartition jointe, théorème de Sklar, familles de copules.
* Illustration des différentes **familles de copules** : Archimédiennes (Clayton, Gumbel), Elliptiques (Gaussienne, t de Student).
* Comparaison visuelle des **structures de dépendance** capturées par chaque copule (queue gauche, queue droite, symétrie).
* Génération de données simulées à partir de copules, avec transformation inverse pour obtenir des marges réelles.
* **Objectif :** comprendre le rôle des copules pour modéliser la dépendance entre variables avec marges quelconques.
---
### 8. `simulation_copules.ipynb`

* Simulation de **copules paramétriques** (Gaussienne, Clayton, Gumbel, Student-t) avec différents niveaux de dépendance.
* Étude des **effets de la dépendance sur les queues extrêmes** : visualisation des densités, contours et nuages de points.
* Comparaison des comportements dans les queues (inférieure, supérieure) pour des valeurs de Kendall’s τ croissantes.
* Intégration d’un cas de **copule empirique** pour modéliser des structures réelles observées dans les données.
* **Objectif :** explorer visuellement et statistiquement l’impact de la copule sur la forme jointe et les risques extrêmes.


## 📄 Rapport de recherche

Un **mémoire de recherche en théorie des valeurs extrêmes (EVT)** accompagne ce travail :  
📌 **"Estimation en théorie des valeurs extrêmes"**  
Il y est question de :
- Fondements mathématiques : probabilités, statistiques d’ordre, quantiles extrêmes ;  
- Lois de valeurs extrêmes (Fréchet, Weibull, Gumbel) et distribution généralisée GEV ;  
- Distribution des excès et loi de Pareto généralisée (GPD) ;  
- Méthodes d’estimation de l’indice de queue γ :  
  - **Non paramétriques** (Hill, Pickands, moments) ;  
  - **Paramétriques** (maximum de vraisemblance, méthode des moments) ;  
- Analyse comparative des estimateurs et discussion sur leur précision et leurs limites.  

👉 Objectif : fournir une base théorique et pratique solide pour la modélisation du risque extrême, avec des applications directes en finance (VaR, ES), en assurance, hydrologie et climatologie.


📎 [Voir le rapport de recherche (PDF)](https://github.com/newma2n/extreme_values_theories/blob/main/Rapport_de_recherche_EVT.pdf)

---

## 🎓 Certification

Projet amorcé dans le cadre d’un cours spécialisé en détection d’anomalies en utilisant la théorie de svaleurs extrêmes:  
**📘 Practical Anomaly Detection**  
🏛️ *appliedAI Institute for AI gGmbH*

📜 [Voir le certificat](https://github.com/newma2n/extreme_values_theories/blob/main/Certificate_of_Completion.pdf)

---

## 🛠️ Stack technique

* Python, Jupyter, NumPy, SciPy, Matplotlib, Seaborn
* `scipy.stats.genextreme`, `copulas`, `statsmodels`
* Visualisation interactive avec `matplotlib.pyplot` et `seaborn`

---

## 🙋‍♂️ Auteur

**Hamidou Kane**  
🎯 **À propos**

Étudiant en mathématiques appliquées, passionné par la modélisation statistique, l’analyse du risque et la finance quantitative.  
📧 [hamidou.kane19@inphb.ci](mailto:hamidou.kane19@inphb.ci)  
📞 +33 7 80 84 75 92  
🔗 [GitHub](https://github.com/newma2n)

---
.
