# Cahier des charges — Module 1 : Gestion des élèves et inscriptions
# 1. Objectif

Permettre à l'administration d'un établissement scolaire :

d'enregistrer un nouvel élève ;
d'enregistrer son tuteur ;
de gérer son dossier administratif ;
de créer son inscription annuelle ;
de l'affecter à une classe ;
de gérer sa réinscription les années suivantes.
# 2. Acteurs concernés
Directeur

Peut :

consulter les élèves ;
consulter les inscriptions ;
superviser les opérations.
Secrétaire

Peut :

créer un élève ;
modifier un élève ;
créer une inscription ;
réinscrire un élève ;
consulter les dossiers.
# 3. Processus d'inscription
Nouvel élève
1. Création du dossier élève
2. Création du tuteur
3. Génération automatique du matricule
4. Vérification des documents présentés
5. Sélection de l'année scolaire
6. Affectation à une classe
7. Validation de l'inscription
4. Informations de l'élève
Identité
Matricule (généré automatiquement)
Nom
Prénom
Sexe
Date de naissance
Lieu de naissance
Adresse
Photo
Photo facultative lors de la création
Ajout possible ultérieurement
# 5. Informations du tuteur

Pour le MVP :

1 élève
↓
1 tuteur

Informations :

Nom
Prénom
Téléphone
Adresse
Lien avec l'élève

Exemples :

Père
Mère
Tuteur
# 6. Documents administratifs

Le système ne stocke pas encore les fichiers.

Il enregistre uniquement si le document a été présenté.

Exemples :

Acte de naissance
Photos
Livret scolaire
Attestation d'entrée en 7ème
BEPC

Statuts :

Présenté
Non présenté
# 7. Gestion du dossier

Un dossier peut être :

Complet
Incomplet

L'inscription reste possible même avec un dossier incomplet.

# 8. Inscription annuelle

Une inscription contient :

Année scolaire
Cycle
Niveau
Série (si lycée)
Classe

Exemple :

2026-2027
↓
Collège
↓
7ème année
↓
7ème A
# 9. Réinscription

La réinscription :

conserve le même élève ;
conserve le même matricule ;
crée une nouvelle inscription annuelle.

Exemple :

Mamadou Diallo
Matricule : ELV-0001

2026-2027 → 7ème A
2027-2028 → 8ème B
2028-2029 → 9ème A
# 10. Cas particuliers
Passage en classe supérieure

Nouvelle inscription.

Redoublement

Nouvelle inscription dans le même niveau.

Départ de l'établissement

L'élève quitte l'école.

Fin de cycle

L'élève termine son parcours dans l'établissement.

Abandon

Le dossier est conservé.
# Nous pouvons maintenant verrouiller les tables du Module 1

Je propose :

Etablissement
AnneeScolaire

Cycle
Niveau
Serie
Classe

Tuteur
Eleve

Inscription

# Relations métier
Etablissement
      ↓
AnneeScolaire

Etablissement
      ↓
Cycle
      ↓
Niveau
      ↓
Serie
      ↓
Classe

Tuteur
      ↓
Eleve
      ↓
Inscription
      ↓
Classe
      ↓
AnneeScolaire

# Décisions importantes validées
Élève ≠ Inscription
Historique scolaire conservé
Réinscription = nouvelle inscription
Matricule généré automatiquement
Photo téléversée dans le dossier élève
Un seul tuteur pour le MVP
Documents administratifs :
Acte de naissance
Livret scolaire
Attestation 7ème
BEPC
etc.
gérés par des champs de présence (Oui/Non)
Élève jamais supprimé
Statuts possibles :
Actif
Ancien élève
Abandonné
Diplômé
Transféré