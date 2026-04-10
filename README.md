# Bus Schedule App

Compte Rendu : Application Bus Schedule avec Room Database
1. Introduction
L'objectif de cette application Android est d'afficher les horaires des bus à partir d'une base de données locale Room. L'utilisateur peut voir la liste des arrêts de bus et sélectionner un arrêt pour afficher les heures d'arrivée correspondantes.
2. Dépendances utilisées
Les dépendances Room ont été ajoutées dans le fichier build.gradle :
implementation("androidx.room:room-ktx:2.5.1")
implementation("androidx.room:room-runtime:2.5.1")
ksp("androidx.room:room-compiler:2.5.1")
3. Création de l'Entity
La classe Schedule est convertie en Room Entity représentant la table de la base de données avec les champs : id, stopName et arrivalTime.
4. Création du DAO
Le DAO permet d'accéder aux données avec deux méthodes principales :
- récupérer tous les horaires triés par heure d'arrivée
- récupérer les horaires d'un arrêt spécifique.
5. Création de la base de données Room
La base de données Room est configurée pour utiliser l'Entity Schedule et le DAO ScheduleDao. Elle est initialisée avec les données présentes dans le fichier assets/database/bus_schedule.db.
6. Mise à jour du ViewModel
Le ViewModel récupère les données depuis le DAO et les expose à l'interface utilisateur via des Flow ou LiveData. Cela permet d'afficher dynamiquement les horaires des bus.
7. Résultat de l'application

<img width="1800" height="942" alt="Capture d&#39;écran 2026-04-10 210728" src="https://github.com/user-attachments/assets/2b6f59d9-5b0a-4115-8067-e4ecd4100b0e" />

