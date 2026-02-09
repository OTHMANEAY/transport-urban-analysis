🚍 Analyse du Ridership des Transports Urbains
Chicago & Philadelphie

Power BI • Python (ETL) • Data Analytics • Aide à la décision

📌 Contexte du projet

Ce projet vise à analyser la fréquentation (ridership) des réseaux de transport urbain de Chicago et Philadelphie à partir de données historiques multi-sources.

L’objectif principal est de construire un dashboard Power BI interactif, pensé pour la prise de décision, permettant de :

analyser l’évolution du trafic dans le temps,

comparer les performances entre villes, modes et routes,

détecter les segments instables ou sous-performants,

fournir des éléments concrets d’aide à la décision stratégique.

🎯 Enjeux métier

Les réseaux de transport urbain sont caractérisés par une forte variabilité de la demande selon :

la ville,

le mode de transport (bus, rail, etc.),

les routes ou lignes spécifiques.

Sans une analyse structurée, les agences rencontrent des difficultés à :

anticiper les variations de fréquentation,

optimiser l’allocation des ressources,

identifier les routes à faible performance,

comparer objectivement les performances entre villes.

Ce projet répond à ces enjeux via une approche data-driven.

🛠️ Technologies utilisées

Python : ETL & préparation des données

pandas : nettoyage, standardisation et contrôles qualité

Power BI Desktop : visualisation et modélisation

Modèle en étoile

DAX : mesures et KPIs

Dashboards interactifs orientés décision

🔧 Préparation & traitement des données (ETL)

Les données provenant de sources hétérogènes ont été traitées via un pipeline Python afin de garantir leur cohérence avant intégration dans Power BI.

Étapes clés :

Chargement et consolidation des données (Chicago / Philadelphie)

Uniformisation des champs :
Année, Mois, Ville, Mode, Route, Ridership

Nettoyage des données :

suppression des doublons,

gestion des valeurs manquantes,

correction des types et formats

Harmonisation inter-villes pour assurer la comparabilité

Export des tables finales vers data/processed/*.csv

Contrôles qualité appliqués :

validation des clés temporelles et métiers,

vérification de la complétude par ville et période,

détection d’anomalies (valeurs nulles incohérentes, négatifs).

🗂️ Modélisation des données (Power BI)

Le modèle analytique repose sur un schéma en étoile, favorisant la lisibilité et la performance.

Tables de faits :

Fait_Mode : ridership agrégé par mode

Fait_Route : ridership détaillé par route

Dimensions :

Dim_City

Dim_Mode

Dim_Route

Dim_Mois

Dim_Année

Mesures :

Table dédiée DAX_Measures pour centraliser les KPIs.

📊 Organisation du dashboard
🔹 Page 1 — Vue globale

Objectif : compréhension rapide de la dynamique du trafic.

Ridership total

Évolution temporelle (Chicago vs Philadelphie)

Répartition par mode et par ville

Indicateurs de volatilité

Suivi des objectifs

🔹 Page 2 — Analyse performance & stabilité

Objectif : identifier les forces et faiblesses opérationnelles.

Part des modes et des routes

Top 10 / Bottom 10 routes

Analyse de la volatilité

Matrice Performance vs Volatilité pour appui décisionnel

🔹 Page 3 — Benchmark inter-villes

Objectif : comparaison directe Chicago / Philadelphie.

KPIs comparatifs et écarts

Évolution temporelle croisée

Différences de structure par mode

Analyse comparative de la stabilité

📈 Indicateurs clés (KPIs)

Ridership total (Mode / Route)

Parts relatives (%)

Variation mensuelle (MoM)

Volatilité (écart-type)

Routes les plus / moins performantes

Performance vs Volatilité

Écart Chicago vs Philadelphie (valeur & %)

💡 Enseignements & recommandations

Piloter la stratégie prioritairement au niveau des modes (impact volume)

Optimiser les routes sous-performantes (fréquence, priorisation)

Surveiller les segments à forte volatilité pour améliorer la stabilité

Adapter les décisions selon les spécificités de chaque ville

Utiliser le benchmark inter-villes comme levier d’amélioration continue

📁 Structure du dépôt
Analyse-des-performances-et-satisfaction-des-transports-urbains/
data/
    processed/ # Données nettoyées prêtes pour Power BI
    row/# Notebooks Python (ETL, nettoyage, contrôles)   
PowerBI_Dashboard.pbix
README.md
