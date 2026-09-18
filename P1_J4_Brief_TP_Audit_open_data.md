# TP — Auditer un jeu de données open data

|                      |                                                                                 |
| -------------------- | ------------------------------------------------------------------------------- |
| **Semaine**          | P1 (S38) · Socle · jeudi 17/09/2026, 15h00–16h30                                |
| **Compétence visée** | **C1.1** — Identifier les usages possibles des données et en évaluer la qualité |
| **Niveau visé**      | **1 · Imiter** (reproduire la démarche montrée en démo)                         |
| **Évaluation**       | Formative                                                                       |
| **Outils**           | Tableur (Excel ou LibreOffice), navigateur, Git/GitHub                          |
| **Prérequis**        | Tri, filtre, mise en forme conditionnelle (mardi) · dépôt, commit (lundi)       |
| **Alimente**         | Livrable du vendredi 18/09 : _Repo GitHub + première analyse commentée_         |

## Contexte

Vous venez d'être recruté·e comme Data Analyst dans une agence de développement économique du Pas-de-Calais. Avant de lancer toute analyse, votre responsable veut savoir si les données publiques disponibles sont fiables et à quoi elles pourraient servir.

## Choisir son parcours

**Parcours socle** — pour celles et ceux qui découvrent le tableur ou l'analyse de données.
Jeu imposé sur data.gouv.fr : _Prix des carburants en France — flux instantané_ (export CSV). Filtrez sur le département 62.

**Parcours +** — pour celles et ceux qui ont déjà manipulé des données.
Jeu libre sur data.gouv.fr ou insee.fr, en lien avec le territoire (Hauts-de-France). Faites en plus l'étape 5.

## Étapes

### 1. Lire la fiche du jeu (15 min)

Complétez le tableau d'identité ci-dessous **avant** d'ouvrir le fichier.

| Élément                                           | Votre réponse |
| ------------------------------------------------- | ------------- |
| Titre du jeu                                      |               |
| Producteur                                        |               |
| URL                                               |               |
| Licence                                           |               |
| Date de dernière mise à jour                      |               |
| Fréquence de mise à jour                          |               |
| Couverture géographique et temporelle             |               |
| Format téléchargé                                 |               |
| Dictionnaire des variables disponible ? (oui/non) |               |

### 2. Ouvrir et décrire (15 min)

- Nombre de lignes et de colonnes.
- Pour 5 colonnes au choix : nom, type de valeur (texte, nombre, date), exemple de valeur.
- Signalez tout problème d'ouverture (séparateur, accents mal affichés, dates en texte).

### 3. Remplir la grille qualité (35 min)

Pour chaque dimension, donnez **au moins un constat chiffré ou un exemple précis** (ligne, colonne, valeur).

| Dimension  | Méthode utilisée dans le tableur              | Constat (chiffré ou exemple) | Gravité (faible / moyenne / forte) |
| ---------- | --------------------------------------------- | ---------------------------- | ---------------------------------- |
| Complétude | `NB.VIDE`, filtre sur _(Vides)_               |                              |                                    |
| Exactitude | Tri, `MIN` / `MAX`, valeurs implausibles      |                              |                                    |
| Cohérence  | Comparaison entre deux colonnes liées         |                              |                                    |
| Validité   | Filtre : formats hétérogènes dans une colonne |                              |                                    |
| Unicité    | MFC _Valeurs en double_ sur l'identifiant     |                              |                                    |
| Fraîcheur  | Date la plus récente vs date du jour          |                              |                                    |

### 4. Proposer des usages (15 min)

Proposez **deux usages** de ce jeu pour l'agence. Pour chacun :

- la question métier à laquelle il répond ;
- la ou les colonnes utilisées ;
- le défaut qualité qui pourrait fausser la réponse.

### 5. Parcours + uniquement : croiser deux sources (en autonomie)

Trouvez une seconde source pour un même indicateur (ex. population communale INSEE vs portail régional). Comparez les valeurs sur 5 lignes et expliquez les écarts éventuels.

### 6. Versionner (10 min)

Dans votre dépôt GitHub :

- ajoutez la grille et vos notes dans un fichier `audit_qualite.md` ;
- faites au moins un commit avec un message explicite (ex. `Ajout grille qualité carburants 62`).

## Critères de réussite (C1.1 · niveau 1)

- [ ] La fiche d'identité est complète : source, licence et date de mise à jour sont renseignées.
- [ ] Les 6 dimensions de la grille sont renseignées, chacune avec un constat précis.
- [ ] Au moins deux usages sont proposés et reliés à des colonnes réelles du jeu.
- [ ] Le travail est commité sur GitHub.

## Ressources

- data.gouv.fr — portail national des données publiques
- insee.fr — statistiques officielles
- Slides de la séance : _Panorama de la donnée & open data_
