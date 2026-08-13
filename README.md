\# Sales Dashboard - Power BI



Dashboard interactif d'analyse des ventes construit avec Power BI, basé sur le dataset "Sample Superstore" (9 994 lignes, 2014-2017, ventes US).



\## Objectif



Permettre à un manager d'explorer les ventes par période, région, produit et catégorie client, avec des KPIs clés et des visuels interactifs.



\## Structure du projet



\- `data/` : dataset nettoyé et structuré en modèle en étoile (Fact\_Sales + 4 tables de dimension)

\- `Sales\\\\\\\_Dashboard.pbix` : fichier Power BI complet

\- `Sales\\\\\\\_Dashboard\\\\\\\_Export.pdf` : export PDF du dashboard

\- `DAX\\\\\\\_measures.md` : documentation de toutes les mesures DAX utilisées



\## Modélisation des données



Modèle en étoile avec :

\- \*\*Fact\_Sales\*\* : table de faits (ventes ligne par ligne)

\- \*\*Dim\_Customer\*\*, \*\*Dim\_Product\*\*, \*\*Dim\_Location\*\*, \*\*Dim\_Date\*\* : tables de dimension

\- Dim\_Date créée via `CALENDAR()` en DAX, marquée comme table de dates officielle



\## KPIs et mesures



\- CA Total, Profit Total, Marge %, Panier Moyen, Nombre de commandes

\- Croissance Mois-sur-Mois (MoM) et Année-sur-Année (YoY)

\- Cumul annuel (YTD)



Détail complet dans \[DAX\_measures.md](./DAX\_measures.md).



\## Pages du dashboard



\*\*Page 1 - Vue d'ensemble\*\* : KPIs principaux, évolution du CA dans le temps, top sous-catégories, carte des ventes par État, filtres Région/Année.



\*\*Page 2 - Détail\*\* : tableau détaillé par catégorie/sous-catégorie (CA, profit, marge), graphique de profitabilité par sous-catégorie.



\## Insights clés



\- Les sous-catégories \*\*Tables\*\*, \*\*Bookcases\*\* et \*\*Supplies\*\* ont un profit négatif malgré des ventes significatives, probablement lié à des remises excessives.

\- Le CA suit une forte saisonnalité, avec des pics récurrents en fin d'année (novembre-décembre).

\- \*\*Phones\*\* et \*\*Chairs\*\* sont les sous-catégories les plus performantes en chiffre d'affaires.



\## Outils utilisés



Power BI Desktop, Power Query, DAX

