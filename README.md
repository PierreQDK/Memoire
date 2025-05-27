# 📘 Impact de la novation sur les marchés à terme agricoles – Cas du CBOT (1926)

Projet réalisé dans le cadre du Master 1 Économétrie et Statistiques – parcours Économétrie Appliquée (IAE de Nantes).

## 📌 Objectif

Ce projet vise à évaluer l'impact de la mise en place de la **novation** au **Chicago Board of Trade (CBOT)** en février 1926, en analysant ses effets sur les marchés à terme agricoles (blé et maïs).

Les effets sont étudiés à travers plusieurs dimensions :
- Prix de clôture
- Volatilité
- Engagements contractuels (Open Interest)
- Flux physiques (Receipts & Shipments)
- Spreads entre places de marché (Chicago, Kansas City, St. Louis)

## 📁 Données

Les données utilisées proviennent d’archives historiques et ont été saisies manuellement :
- **daily_futures_prices_1920s.xlsx** : prix quotidiens des contrats à terme.
- **Dataset1920_ln.xlsx** : volumes physiques (livraisons et expéditions).
- **open_commitment_1920s.xlsx** : engagement contractuel par ville.
- Période d’observation : 1924 à 1927.

## 🛠 Méthodologie

- Nettoyage et traitement des données (dates, doublons, valeurs aberrantes via RosnerTest)
- Statistiques descriptives et visualisation des prix
- Tests de tendances parallèles (pré-traitement)
- Modélisation économétrique :
  - **Diff-in-Diff** (TWFE avec erreurs robustes)
  - **Synthetic DiD** (avec `synthdid`)
- Comparaison des spreads et de la volatilité avant/après la réforme
- Estimation des effets sur l’Open Interest, les Receipts et Shipments

## 🧠 Résultats

- 📈 Les prix des contrats à terme augmentent significativement à Chicago après l’introduction de la novation.
- 📉 L’Open Interest diminue à court terme, indiquant une possible frilosité des opérateurs face à la réforme.
- 🌍 Réduction des spreads entre Chicago et les autres villes → meilleure intégration du marché.
- 📦 Aucun effet clair sur les volumes physiques échangés.

## 💻 Technologies utilisées

- Langage : **R**
- Packages :  
  `dplyr`, `ggplot2`, `plm`, `broom`, `synthdid`, `readxl`,  
  `DescTools`, `e1071`, `lubridate`, `tidyverse`, `rosnerTest`, `stargazer`, `performance`


## 👤 Auteur

- **Pierre Quintin de Kercadio**  



