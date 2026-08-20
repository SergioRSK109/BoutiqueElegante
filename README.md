# ELEGANTE BOUTIQUE — App de gestion

Application de gestion de boutique (ventes, stock, pertes, précommandes)
avec catalogue client public, hébergée gratuitement sur GitHub Pages et
connectée à Firebase (Firestore + Authentication).

## Structure du projet

- `interne.html` — application interne pour l'équipe (tableau de bord,
  ventes, stock, pertes, précommandes, historique, export CSV). Accès
  protégé par connexion (email/mot de passe Firebase Authentication).
- `catalogue.html` — catalogue public pour les clientes (parcourir les
  articles, précommander, choisir un mode de paiement, générer une
  facture WhatsApp/imprimable). Accès libre, sans connexion.
- `logo.png` — logo de la boutique, utilisé dans les deux pages.

## Liens en production

- Interne (équipe uniquement) : https://sergiorsk109.github.io/BoutiqueElegante/interne.html
- Catalogue (public) : https://sergiorsk109.github.io/BoutiqueElegante/catalogue.html

## Configuration technique requise

- Projet Firebase "boutiqueelegante" avec Firestore Database et
  Authentication (méthode Email/Mot de passe) activés
- La configuration Firebase (firebaseConfig) est déjà intégrée dans les
  deux fichiers HTML
- Règles de sécurité Firestore : voir section "Sécurité" ci-dessous
- Upload photo des articles : via l'API imgbb (clé API intégrée dans le
  code de interne.html)

## Comptes utilisateurs (équipe)

Les comptes de connexion à interne.html se gèrent depuis la console
Firebase > Authentication > Users > Add user (email + mot de passe).

## Sécurité

- Lecture publique du catalogue et des réglages (nom boutique, adresse,
  numéros de paiement)
- Écriture (stock, ventes, pertes, validation de précommandes) réservée
  aux comptes connectés
- N'importe qui peut créer une précommande depuis le catalogue, mais
  seule l'équipe peut la consulter ou la modifier

## Modifications futures

Pour toute modification, fournir ce dépôt et les fichiers concernés à
Claude Code, avec une description précise du changement souhaité.
