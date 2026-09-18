| Élément                                           | Votre réponse                                                                                                                                 |
| ------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Titre du jeu                                      | Prix des carburants en France - Flux instantané - v2                                                                                          |
| Producteur                                        | Ministère économique et financiers                                                                                                            |
| URL                                               | https://www.data.gouv.fr/datasets/prix-des-carburants-en-france-flux-instantane-v2-amelioree?resource_id=edd67f5b-46d0-4663-9de9-e5db1c880160 |
| Licence                                           | Licence ouverte/Open licence version 2.0                                                                                                      |
| Date de dernière mise à jour                      | 18 septembre 2026                                                                                                                             |
| Fréquence de mise à jour                          | Toutes les dix minutes                                                                                                                        |
| Couverture géographique et temporelle             | France entière en temps réele mise a jour toute les 10 minutes                                                                                |
| Format téléchargé                                 | csv                                                                                                                                           |
| Dictionnaire des variables disponible ? (oui/non) | oui                                                                                                                                           |

## 2. Ouvrir et décrire

Il y a 47 colonnes et 231 lignes

### Description de 5 colonnes

| Nom                    | Type de valeur | Exemple                                                                                                                      |
| ---------------------- | -------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Ville                  | Texte          | Arras                                                                                                                        |
| Prix E10 mis à jour le | Date/heure     | 2026-08-27T10:58:49+00:00                                                                                                    |
| id                     | Nombre         | 62880001                                                                                                                     |
| Adresse                | Texte          | 43 BOULEVARD DE LA LIANE                                                                                                     |
| Services proposés      | Texte          | Toilettes publiques,Boutique alimentaire,Bar,Carburant additivé,Piste poids lourds,Vente de gaz domestique (Butane, Propane) |

# Problèmes constatés

Il n'y a pas de problème d'ouverture, de séparateur, d'accents mal affichés et de dates en texte.

## 3. Remplir la grille qualité

| Dimension  | Méthode utilisée dans le tableur              | Constat (chiffré ou exemple)                                                                                                      | Gravité (faible / moyenne / forte) |
| ---------- | --------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------- |
| Complétude | `NB.VIDE`, filtre sur _(Vides) _              | 9 cellules vides sur 231 lignes dans la colonne « Carburants disponibles ».                                                       | Faible                             |
| Exactitude | Tri, `MIN` / `MAX`, valeurs implausibles      | Prix du Gazole est entre 2,40 € à 2,802 €.                                                                                        | Faible                             |
| Cohérence  | Comparaison entre deux colonnes liées         | Comparaison entre les colonnes « Prix Gazole » et « Prix Gazole mis à jour le » a chaque que l'un a été mise a jour l'autre aussi | Faible                             |
| Validité   | Filtre : formats hétérogènes dans une colonne | Les valeurs de la colonne sont enregistrées au même format numérique.constaté.                                                    | Faible                             |
| Unicité    | MFC _Valeurs en double_ sur l'identifiant     | Aucun identifiant en double détecté parmi les données du département 62.                                                          | Faible                             |
| Fraîcheur  | Date la plus récente vs date du jour          | La date de mise à jour la plus récente des prix du gazole est le 18/09/2026 à 09:30                                               | Faible                             |

## 4. Proposer des usages

### Usage 1 : Trouver les stations les moins chères

- **Question métier :** Quelles sont les differences de prix du carburant dans les differentes villes du Pas-de-Calais?
- **Colonnes utilisées :** Ville, Prix.
- **Défaut qualité pouvant fausser la réponse :** il manque la mise a jour sur le prix pour certain carburant.

### Usage 1 : Services dans les stations

- **Question métier :** Quels sont le differents services proposés par les stations du Pas-de-Calais
- **Colonnes utilisées :** villes, services proposé
- **Défaut qualité pouvant fausser la réponse :** Les services sont regroupper dans une cellule, difficile de les comparer.
