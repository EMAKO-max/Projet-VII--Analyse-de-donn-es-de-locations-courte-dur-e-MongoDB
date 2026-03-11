N.B Toutes les tâches réalisées dans ce projet sont capturer dans le PDF attaché.
                                                               
                                                               Analyse de données de locations courte durée – MongoDB
                                    I.  Contexte

Ce projet a été réalisé dans le cadre d'un exercice de Data Engineering pour l'association NosCités.

NosCités analyse l'impact des plateformes de location de courte durée sur l'offre de logements dans plusieurs villes françaises, notamment Paris et Lyon. L'objectif est d'apporter de la transparence dans le débat public concernant l'influence de ces plateformes sur le marché immobilier.

Lors d'un incident technique, la base de données contenant les informations sur les locations à Paris a subi un crash complet. Une sauvegarde des données a été retrouvée mais sa fiabilité doit être vérifiée.

Le rôle du Data Engineer est donc de :

                                      - restaurer la base de données MongoDB,

                                      - analyser l'intégrité des données,

                                      - garantir la pérennité du système de stockage.

Ces analyses permettront de produire un rapport sur l’impact des Jeux Olympiques 2024 sur l’offre de logements à Paris.

Outils Utilisées
          
           - MongoDB (mongocompass)
           - Pymongo
           - Polars
           - Power BI


                                   II. Objectifs du projet

Le projet est divisé en trois parties principales :

1️⃣ Restaurer la base de données MongoDB
2️⃣ Vérifier l’intégrité et la cohérence des données
3️⃣ Mettre les données  à la disposition de l'équipe de paris.
4️⃣ Mettre en place des pratiques pour éviter de futurs incidents

                                      II.1. Base de données ongoDB restaurée.

        Taches realisées 
                          
                          - Installez MongoDB si ce n’est pas déjà fait.
                          - Importez les données dans une collection MongoDB (MongoCompass).
                              
                                      II.2 Intégrité et  cohérence des données

        Taches realisées & Outils utilisés.

    . Un certain nombre de chiffres (Mongocompass)

- Comptez le nombre de documents de la base de données.
- Comptez le nombre de logements avec des disponibilités. 
- Le nombre d’annonces par type de location
- Les logements les plus loués
- Le nombre total d’hôtes différents
- Le nombre de locations réservables instantanément
- Les hôtes avec plus de 100 annonces sur les plateformes
- Le nombre de super hôtes différents

  . Des statistiques (Pymongo, Polars)

- Le taux de réservation moyen par mois par type de logement
- La médiane des nombre d’avis pour tous les logements (cela nous donne une idée du nombre de réservations pour les logements)
- La médiane des nombres d’avis par catégorie d’hôte (super hôte vs non super hôte)
- La densité de logements par quartier de Paris
- Les quartiers avec le plus fort taux de réservation par mois.

                          II.3 Données  à la disposition de l'équipe de paris.

Tâches réalisées: connecter votre base de données à un outil de business intelligence (Power BI) pour mettre les résultats d’analyse à disposition de l’équipe parisienne de l’association.

                          II.4 Pratiques pour éviter de futurs incidents

Tâches réalisées 
                
                - Repliquer les données avec le ReplicatSet

                - Distribuer les données avec  le Sharding.