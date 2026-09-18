# Voici la version actuelle du README - Module 1 : Gestion des élèves et inscriptions.

# 1 Table Tuteur

    Tuteur
    ------
    id

    nom
    prenom

    telephone

    lien_avec_eleve

    date_creation
    date_modification

# 2 Table Élève

    Eleve
    -----
    id

    matricule

    nom
    prenom

    sexe

    date_naissance
    lieu_naissance

    adresse

    photo

    statut

    tuteur_id

    date_creation
    date_modification

# Statut élève

    Actif
    Ancien élève
    Abandonné
    Diplômé
    Transféré

# 3 Table Inscription

    Inscription
    -----------
    id

    eleve_id

    annee_scolaire_id

    classe_id

    date_inscription

    observation

    date_creation
    date_modification

# 4 Table DocumentEleve

    DocumentEleve
    -------------
    id

    inscription_id

    acte_naissance_presente

    photo_presentee

    livret_scolaire_presente

    attestation_7eme_presentee

    bepc_presente

    dossier_complet

    date_creation
    date_modification

# 5 Table AnneeScolaire

    AnneeScolaire
    -------------
    id

    libelle

    date_debut

    date_fin

    active

    date_creation
    date_modification

# 6 Table Cycle
    Cycle
    ------
    id

    nom

    description

    date_creation
    date_modification

# Status Cycle
    Maternelle
    Primaire
    Collège
    Lycée

# 7 Table Niveau
    Niveau
    -------
    id

    nom

    ordre

    cycle_id

    date_creation
    date_modification

# 8 Table Serie

    Serie
    -----
    id

    nom

    description

    date_creation
    date_modification

# 9 Table Classe

    Classe
    ------
    id

    nom

    niveau_id

    serie_id

    capacite

    date_creation
    date_modification

# 10 Etablissement
-------------
id

nom

fondateur

annee_creation

telephone

logo

date_creation
date_modification