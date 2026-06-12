# Système de Gestion d’Hôtel

## Description
Ce projet consiste à développer une base de données pour la gestion d’un hôtel. Elle permet de gérer les clients, les réservations, les chambres, les séjours et les paiements.

## Objectifs
- Enregistrer les clients.
- Gérer les réservations des chambres.
- Suivre les séjours des clients.
- Gérer les paiements.
- Organiser les chambres selon leur type.

## Structure de la Base de Données

### CLIENT
Contient les informations des clients.

| Attribut | Description |
|-----------|-------------|
| id_client | Identifiant du client |
| nom | Nom du client |
| prenom | Prénom du client |
| telephone | Numéro de téléphone |
| email | Adresse email |

### TYPE_CHAMBRE
Contient les types de chambres disponibles.

| Attribut | Description |
|-----------|-------------|
| id_type | Identifiant du type |
| libelle | Nom du type |
| prix | Prix de la chambre |

### CHAMBRE
Contient les informations des chambres.

| Attribut | Description |
|-----------|-------------|
| id_chambre | Identifiant de la chambre |
| numero | Numéro de la chambre |
| statut | État de la chambre |
| id_type | Type de la chambre |

### RESERVATION
Contient les réservations effectuées par les clients.

| Attribut | Description |
|-----------|-------------|
| id_reservation | Identifiant de la réservation |
| date_reservation | Date de réservation |
| date_arrivee | Date d'arrivée |
| date_depart | Date de départ |
| statut | État de la réservation |
| id_client | Client concerné |
| id_chambre | Chambre réservée |
| id_paiement | Paiement associé |

### PAIEMENT
Contient les paiements réalisés.

| Attribut | Description |
|-----------|-------------|
| id_paiement | Identifiant du paiement |
| date_paiement | Date du paiement |
| montant | Montant payé |
| mode_paiement | Mode de paiement |

### SEJOUR
Contient les séjours réalisés.

| Attribut | Description |
|-----------|-------------|
| id_sejour | Identifiant du séjour |
| date_entree | Date d'entrée |
| date_sortie | Date de sortie |
| id_reservation | Réservation associée |

## Relations
- Un client peut effectuer plusieurs réservations.
- Une réservation concerne une seule chambre.
- Une chambre appartient à un seul type de chambre.
- Une réservation peut générer un paiement.
- Une réservation peut donner lieu à un séjour.

## Technologies Utilisées
- MySQL
- MySQL Workbench
- Modèle Conceptuel de Données (MCD)
- Modèle Logique de Données (MLD)

## Auteur
Projet réalisé dans le cadre d’un exercice de conception et gestion de bases de données.
