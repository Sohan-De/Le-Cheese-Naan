# Cheese Naan Béziers · Template 3

Site vitrine statique pour le Cheese Naan, 14 avenue Saint-Saëns, 34500 Béziers.
HTML5, CSS3 et JavaScript vanilla. Aucun framework, aucun build, aucune dépendance, aucune requête externe à l'exécution.

Direction artistique : fond noir charbon, texte crème, accent flamme orange, typographie grotesque géante et étiquettes en mono. Pas de photo plein écran, pas de cartes arrondies : c'est une affiche éditoriale.

## Structure

```
template-3/
├── index.html
├── mentions-legales.html
├── README.md
└── assets/
    ├── css/styles.css
    ├── js/main.js
    ├── img/
    │   ├── favicon.svg          (fourni)
    │   ├── logo-mark.svg        (fourni)
    │   ├── signature.jpg        (à ajouter)
    │   ├── gallery-1.jpg        (à ajouter)
    │   ├── gallery-2.jpg        (à ajouter)
    │   ├── gallery-3.jpg        (à ajouter)
    │   └── map.jpg              (à ajouter)
    └── fonts/
        ├── space-grotesk-latin-wght-normal.woff2     (à ajouter)
        └── ibm-plex-mono-latin-500-normal.woff2      (à ajouter)
```

## Données déjà renseignées

Source : fiche Google Business (4,6 sur 1 083 avis, €10–20, « Fast food restaurant »).

- Nom, adresse, téléphone : +33 9 60 45 23 36.
- Services : sur place, à emporter, livraison sans contact.
- Statut : « Ouvert · ferme à 1 h » est affiché sur la fiche. Les horaires jour par jour n'étaient pas visibles, donc ils restent à saisir.
- Produit : « Le Poulet », naan burger (poulet pané croustillant, oignons frits, crudités, sauce andalouse), et le menu avec frites et boisson. Tiré du post du propriétaire.
- Avis : 3 avis avec initiales et dates approximatives. Textes traduits du français, à vérifier sur les originaux.

## Placeholders à remplacer

Chaque valeur manquante est en jaune (`.placeholder`). Recherchez `[` dans les fichiers.

**`index.html`**

| Élément | Action |
|---|---|
| Slogan (hero) | `[SLOGAN À COMPLÉTER]` |
| Carte | Reprise de la page Uber Eats (prix Uber Eats). À mettre à jour si les prix changent |
| Horaires | Repris de Uber Eats : 11 h à 1 h tous les jours. À confirmer avec la fiche Google, qui n'affichait que la fermeture à 1 h |
| Boutons « Commander » | Pointent vers la page Uber Eats du snack |
| Réseaux sociaux (pied de page) | Ajouter les liens réels, ou supprimer la ligne |
| Métadonnées | `[URL DU SITE]` dans `og:url` et `og:image` |
| Avis | Les trois avis sont des initiales et des dates approximatives. Ajouter le lien « Voir les avis sur Google » avec l'URL de la fiche |

**`mentions-legales.html`** : toutes les valeurs à compléter sont des `<em class="placeholder">` (forme juridique, SIRET, TVA, directeur de publication, hébergeur, développeur, crédits photos, e-mail RGPD, date).

Le JSON-LD `Restaurant` contient le nom, l'adresse, le téléphone, la gamme de prix et la cuisine. `aggregateRating` est volontairement absent : Google demande que la note structurée corresponde aux avis visibles sur la page, à ajouter une fois les avis réels en place.

## Images à ajouter

| Fichier | Taille recommandée | Usage |
|---|---|---|
| `signature.jpg` | 960 × 1200 px (portrait 4:5) | Photo du naan signature |
| `gallery-1.jpg` | 1200 × 1200 px (carré) | Comptoir |
| `gallery-2.jpg` | 1200 × 1200 px (carré) | Préparation |
| `gallery-3.jpg` | 1200 × 1200 px (carré) | Salle |
| `map.jpg` | 960 × 640 px | Capture statique de la carte (sans iframe) |

Moins de 200 Ko par photo (JPEG, qualité 75 à 80). La page n'a pas d'image plein écran : le hero est typographique. Le navigateur affiche des erreurs 404 dans la console tant que les images ne sont pas ajoutées.

## Polices à télécharger

Les deux polices sont sous licence SIL Open Font License (OFL).

1. **Space Grotesk** (titres) : [fonts.google.com/specimen/Space+Grotesk](https://fonts.google.com/specimen/Space+Grotesk). Télécharger le WOFF2 du sous-ensemble `latin`, axe de graisse variable. Renommer en `space-grotesk-latin-wght-normal.woff2`.
2. **IBM Plex Mono** (étiquettes et prix) : [fonts.google.com/specimen/IBM+Plex+Mono](https://fonts.google.com/specimen/IBM+Plex+Mono). Télécharger le WOFF2 `latin` en graisse 500. Renommer en `ibm-plex-mono-latin-500-normal.woff2`.

Les deux fichiers vont dans `assets/fonts/`. Sans eux, le site utilise Helvetica Neue, Arial et la police monospace du système.

## Aperçu local

- Double-cliquer sur `index.html`.
- Ou depuis ce dossier : `npx serve`.

## Checklist avant mise en ligne

- [ ] Saisir les horaires jour par jour et vérifier le statut un mardi, un dimanche et après minuit
- [ ] Renseigner le lien Uber Eats du bouton « Commander »
- [ ] Remplacer la carte indicative par la carte réelle avec les prix
- [ ] Ajouter les photos (signature, galerie, carte) dans les tailles indiquées
- [ ] Compléter les mentions légales : SIRET, forme juridique, directeur de publication, hébergeur
- [ ] Vérifier les avis sur la fiche Google et ajouter le lien
- [ ] Tester sur un vrai téléphone, en mode portrait et paysage
- [ ] Vérifier qu'aucune erreur 404 n'apparaît dans la console (polices et images)
