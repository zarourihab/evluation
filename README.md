Exercice 1 — Application de gestion de stock
Dans ce TP, nous avons développé une application Java pour gérer le stock d’un magasin de produits informatiques en utilisant Hibernate et Java Persistence API.

L’application permet de gérer quatre entités principales :

Catégorie

Produit

Commande

LigneCommandeProduit

Le projet est organisé en deux couches principales :

1. Couche Persistance :
Création des classes entités, du fichier de configuration application.properties et de la classe HibernateUtil pour la connexion avec la base de données.

2. Couche Service :
Création de l’interface générique IDao et des services pour gérer les opérations sur les entités (ajouter, modifier, supprimer, afficher).

Plusieurs fonctionnalités ont été réalisées :

afficher les produits par catégorie

afficher les produits commandés entre deux dates

afficher les produits d’une commande donnée

afficher les produits dont le prix est supérieur à 100 DH en utilisant une requête nommée

Des programmes de test ont été créés pour vérifier le bon fonctionnement de chaque fonctionnalité
<img width="1920" height="973" alt="Capture d&#39;écran 2026-03-01 151617" src="https://github.com/user-attachments/assets/5c419c87-6474-4604-a123-32149e060044" />
<img width="1920" height="989" alt="Capture d&#39;écran 2026-02-28 170159" src="https://github.com/user-attachments/assets/e13405f5-c211-43d5-8f92-d32b93b30d02" />
<img width="1920" height="1015" alt="Capture d&#39;écran 2026-02-28 170206" src="https://github.com/user-attachments/assets/81ef4ab0-159c-4918-b300-92d99b63192a" />
<img width="1920" height="1003" alt="Capture d&#39;écran 2026-02-28 170221" src="https://github.com/user-attachments/assets/8147ed06-405a-479b-9ff8-d9e60fc468cf" />
<img width="1920" height="1005" alt="Capture d&#39;écran 2026-02-28 170229" src="https://github.com/user-attachments/assets/326114bf-0409-4b93-ae2f-582e7e93561e" />
<img width="1920" height="1003" alt="Capture d&#39;écran 2026-02-28 170235" src="https://github.com/user-attachments/assets/43b0f720-9e68-406e-a790-c215c6fe203d" />
<img width="1920" height="1009" alt="Capture d&#39;écran 2026-02-28 170243" src="https://github.com/user-attachments/assets/afbb1b90-f1ec-4f6d-a743-9abe90b2c13b" />
<img width="1920" height="1024" alt="Capture d&#39;écran 2026-02-28 170300" src="https://github.com/user-attachments/assets/ca343b71-96d9-4579-a4d3-8c81669a5178" />
<img width="1920" height="1026" alt="Capture d&#39;écran 2026-02-28 170321" src="https://github.com/user-attachments/assets/a25e9dea-dc64-4c78-9f4a-14869d6423a7" />
<img width="1920" height="1031" alt="Capture d&#39;écran 2026-02-28 170325" src="https://github.com/user-attachments/assets/1ba25796-8c5d-4c55-ab34-0fbdcb785ce4" />
<img width="1920" height="1020" alt="Capture d&#39;écran 2026-02-28 170338" src="https://github.com/user-attachments/assets/ad402c73-921d-4cc8-a856-01e7c2a05475" />
<img width="1920" height="1013" alt="Capture d&#39;écran 2026-02-28 170346" src="https://github.com/user-attachments/assets/707f6c70-fb34-49f8-a64d-e5022293b8bb" />
Exercice 2 — Application de gestion de projets
1. Contexte

L’application permet à un bureau d’études de suivre le temps passé sur les projets et de calculer les coûts associés. Elle gère les projets, les tâches, les employés, et les relations entre eux.

2. Couche Persistance

Entités JPA créées dans ma.projet.classes :

Projet : id, nom, dateDebut, dateFin

Tache : id, nom, dateDebut, dateFin, prix

Employe : id, nom, prenom, telephone

EmployeTache : association entre Employe et Tache

Configuration Hibernate via application.properties.

Classe HibernateUtil pour gérer la session Hibernate.

3. Couche Service

Interface générique IDao pour les opérations CRUD.

Services implémentés :

ProjetService : gestion des projets et des tâches associées.

TacheService : gestion des tâches, filtrage par prix ou dates.

EmployeService : gestion des employés et de leurs tâches/projets.

EmployeTacheService : gestion des associations Employe ↔ Tache.

4. Fonctionnalités principales

EmployeService :

Afficher les tâches réalisées par un employé.

Afficher les projets gérés par un employé.

ProjetService :

Afficher les tâches planifiées pour un projet.

Afficher les tâches réalisées avec les dates réelles.

TacheService :

Afficher les tâches dont le prix > 1000 DH (requête nommée).

Afficher les tâches réalisées entre deux dates.
<img width="1920" height="927" alt="Capture d&#39;écran 2026-03-01 153715" src="https://github.com/user-attachments/assets/b4c73f88-091c-4ce0-9aff-4c28bee94427" />
<img width="1920" height="978" alt="Capture d&#39;écran 2026-02-28 213126" src="https://github.com/user-attachments/assets/008d5346-9542-4596-a8e1-52dc0d2e5ae3" />
<img width="1920" height="957" alt="Capture d&#39;écran 2026-02-28 213354" src="https://github.com/user-attachments/assets/8ad7ae07-3999-416a-915b-49d2827cb0d1" />
<img width="1920" height="1015" alt="Capture d&#39;écran 2026-02-28 220709" src="https://github.com/user-attachments/assets/50f2bc06-7c62-4ef1-9a81-25319a47df2e" />
<img width="1920" height="964" alt="Capture d&#39;écran 2026-02-28 220712" src="https://github.com/user-attachments/assets/a6df4aea-20dc-4c9c-9569-627880133c90" />
<img width="1920" height="1007" alt="Capture d&#39;écran 2026-02-28 220718" src="https://github.com/user-attachments/assets/31737738-4d00-4b99-b18f-6cba4efa0aa6" />
<img width="1920" height="1018" alt="Capture d&#39;écran 2026-02-28 220722" src="https://github.com/user-attachments/assets/84666ce9-6265-43b8-8c86-e222208f7cf8" />
<img width="1920" height="1024" alt="Capture d&#39;écran 2026-02-28 220735" src="https://github.com/user-attachments/assets/c975d1f8-adc3-45b4-b4bc-79039d68869e" />
<img width="1920" height="1003" alt="Capture d&#39;écran 2026-02-28 220744" src="https://github.com/user-attachments/assets/063adbf1-a55a-4e29-a7b8-8e72ba693f51" />
<img width="1920" height="1003" alt="Capture d&#39;écran 2026-02-28 220748" src="https://github.com/user-attachments/assets/0aeff91d-e4cc-4404-ae00-d8697ae0db7e" />
<img width="1920" height="1020" alt="Capture d&#39;écran 2026-02-28 220757" src="https://github.com/user-attachments/assets/13183926-5217-46b9-91f9-8570ae5d0ed3" />
<img width="1920" height="1007" alt="Capture d&#39;écran 2026-02-28 220800" src="https://github.com/user-attachments/assets/ae7c2944-8f17-4a80-8e92-8814c8e6d349" />
<img width="1920" height="1018" alt="Capture d&#39;écran 2026-02-28 221432" src="https://github.com/user-attachments/assets/ba08494b-f774-4ddf-b640-296ea12dedf3" />
<img width="1920" height="1013" alt="Capture d&#39;écran 2026-02-28 221439" src="https://github.com/user-attachments/assets/0931ce3e-7c06-4100-925f-01b1c2f16367" />
<img width="1920" height="1011" alt="Capture d&#39;écran 2026-02-28 221449" src="https://github.com/user-attachments/assets/f9d0c2b9-db34-4660-b583-0deaed382ab0" />
<img width="1920" height="1011" alt="Capture d&#39;écran 2026-02-28 221449" src="https://github.com/user-attachments/assets/b9239b0b-ce20-4023-9fc2-be250ffa8779" />
<img width="1920" height="1015" alt="Capture d&#39;écran 2026-02-28 221502" src="https://github.com/user-attachments/assets/c2c5cce5-0039-4ed3-890a-6a1fa445266b" />
Exercice 3 — Application de gestion de projets
1. Couche Persistance

Entités JPA à créer dans ma.projet.beans :

Personne : id, nom, prenom, telephone, adresse, dateNaissance

Homme (hérite de Personne)

Femme (hérite de Personne)

Mariage : dateDebut, dateFin, nbrEnfant

Configuration :

Fichier application.properties pour MySQL.

Classe HibernateUtil pour gérer la session Hibernate.

Génération : Créer automatiquement la base de données MySQL à partir des entités.

2. Couche Service

Interface générique : IDao dans ma.projet.dao.

Services à implémenter :

HommeService

Méthode pour afficher les épouses d’un homme entre deux dates.

Méthode pour afficher les mariages d’un homme donné avec détails (femme, dates, nombre d’enfants).

FemmeService

Méthode utilisant une requête native : nombre d’enfants d’une femme entre deux dates.

Méthode avec une requête nommée : femmes mariées au moins deux fois.

MariageService

Méthode utilisant Criteria API : nombre d’hommes mariés à quatre femmes entre deux dates.

3. Programme de test

Créer 10 femmes et 5 hommes.

Afficher :

Liste des femmes.

Femme la plus âgée.

Épouses d’un homme donné.

Nombre d’enfants d’une femme entre deux dates.

Femmes mariées deux fois ou plus.

Hommes mariés à quatre femmes entre deux dates.

Mariages d’un homme avec tous les détails
<img width="1920" height="916" alt="Capture d&#39;écran 2026-02-28 223303 - Copie" src="https://github.com/user-attachments/assets/b0cb830d-e2bf-4d90-b08a-56283b04457e" />
<img width="1920" height="1035" alt="Capture d&#39;écran 2026-02-28 223343" src="https://github.com/user-attachments/assets/971f5d1c-4281-43fd-a65d-9759bcaf2357" />
<img width="1920" height="1013" alt="Capture d&#39;écran 2026-02-28 223347 - Copie (3)" src="https://github.com/user-attachments/assets/554f38a1-2331-4c4a-bbce-38025edc0771" />
<img width="1920" height="1013" alt="Capture d&#39;écran 2026-02-28 223347 - Copie" src="https://github.com/user-attachments/assets/f1e3f17b-00c2-4933-9e42-69090c34b127" />
<img width="1920" height="1022" alt="Capture d&#39;écran 2026-02-28 223347" src="https://github.com/user-attachments/assets/c13a7743-dafc-4011-933e-75ed06c15b84" />
<img w<img width="1920" height="1011" alt="Capture d&#39;écran 2026-02-28 223410" src="https://github.com/user-attachments/assets/2b9c348d-dc4e-4d22-b6ca-ab0c46638db2" />
idth="1920" height="1022" alt="Capture d&#39;écran 2026-02-28 223353" src="https://github.com/user-attachments/assets/bd37e403-6887-40a6-8e91-eae00b971717" />
<img width="1920" height="1022" alt="Capture d&#39;écran 2026-02-28 223414" src="https://github.com/user-attachments/assets/49c79f92-cb80-451a-b904-3adcbde8927c" />
<img width="1920" height="1020" alt="Capture d&#39;écran 2026-02-28 223421" src="https://github.com/user-attachments/assets/84f2867c-c10e-4415-9df0-c15e8210800d" />
<img width="1920" height="1022" alt="Capture d&#39;écran 2026-02-28 223428" src="https://github.com/user-attachments/assets/7647450b-24fc-4c5c-b5fb-3874b369c706" />
<img width="1920" height="1022" alt="Capture d&#39;écran 2026-02-28 223435" src="https://github.com/user-attachments/assets/bec66ff7-20a9-4e99-95ee-3628fc9c336a" />
<img width="1920" height="992" alt="Capture d&#39;écran 2026-02-28 223438" src="https://github.com/user-attachments/assets/da99595f-f6b6-46d9-a39c-be9ba910c886" />

