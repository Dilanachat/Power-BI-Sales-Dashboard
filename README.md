
## Objectif
Ce projet Power BI a été réalisé dans le cadre d'un projet perso de data visualisation et d’analyse des ventes.  
L’objectif était de construire un tableau de bord interactif à partir d’un fichier CSV, en passant par les étapes de préparation des données, modélisation, création de mesures DAX et conception de visualisations métier.  

## Dataset
Le projet repose sur un fichier de ventes contenant notamment :
- Id commande
- Id client / Nom client
- Id produit / Nom produit / Catégorie produit
- Id région / Nom région
- Date commande
- Quantité
- Prix unitaire
- Prix total
- Statut commande

## Préparation des données
Les traitements ont été réalisés dans Power Query :
- Vérification de la qualité, distribution et du profil des colonnes
- Correction des types de données
- Renommage des colonnes avec des libellés explicites
- Création de tables de référence :
  - Clients
  - Produits
  - Régions
- Création de la table de faits Ventes

## Modèle de données
Le modèle de données a été structuré autour des tables suivantes :
- Ventes
- Clients
- Produits
- Régions

Les relations entre les tables ont été vérifiées et ajustées dans la vue Modélisation de Power BI.

## Mesures DAX
Mesures principales créées :
- Total ventes = `SUM(Ventes[Prix total])`
- Nombre de commandes = `DISTINCTCOUNT(Ventes[Id commande])`
- Quantité vendue = `SUM(Ventes[Quantité])`
- Commande moyenne = `DIVIDE([Total ventes], [Nombre de commandes])`

Mesures complémentaires sur les commandes annulées :
- Total commandes annulées
- Montant commandes annulées
- Pourcentage commandes annulées

## Tableau de bord
### Page 1 — Suivi des ventes
- KPI : total ventes, nombre de commandes, quantité vendue, commande moyenne
- Analyse de l’évolution du chiffre d’affaires et des volumes dans le temps
- Répartition du CA par région
- Répartition du CA par catégorie de produit
- Tableau détaillé des commandes
- Filtres sur la date, le statut de commande et la région

### Page 2 — Commandes annulées
- KPI sur les commandes annulées
- Évolution du pourcentage et du nombre de commandes annulées
- Répartition par région
- Treemap par catégorie et produit
- Analyse trimestrielle par produit

## Fonctionnalités avancées
- Navigation entre les pages via un menu latéral
- Tooltips personnalisés
- Bookmarks pour filtres rapides
- Rôles de sécurité (Row-Level Security)
- Version mobile du rapport
- Publication sur Power BI Service

## Aperçu
Ajoutez ici vos captures d’écran du rapport :

![Dashboard ventes](assets/dashboard-ventes.png)
![Dashboard annulations](assets/dashboard-annulations.png)

## Compétences mobilisées
- Power BI
- Power Query
- DAX
- Modélisation de données
- Data Visualization
- Row-Level Security
- Power BI Service

## Auteur
Tongnia Chatelain
