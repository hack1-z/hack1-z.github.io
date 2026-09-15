# Site CCAZ.SEC, mode d'emploi

Trois fichiers, à déposer ensemble à la racine de votre dépôt GitHub.

- `index.html` : le site public. Tout est inclus (styles, photo, polices de secours). Google Analytics est actif (G-LJ5E871494).
- `projets.json` : la liste des projets affichés dans la section « Projets ». C'est le seul fichier à modifier pour mettre le site à jour.
- `admin.html` : l'écran d'administration protégé par code.

## Mise en ligne

1. Dépôt GitHub > Add file > Upload files > déposez les trois fichiers.
2. Settings > Pages > Source : branche `main`, dossier `/root`.
3. Le site est en ligne sur `https://<votre-utilisateur>.github.io/<depot>/`.

## Mettre à jour les projets

Ouvrez `https://<votre-site>/admin.html`, saisissez le code (par défaut **CCAZ-2026**, à changer dès la première connexion en bas de page).

Deux façons de publier :

- **Simple** : bouton « Télécharger projets.json », puis remplacez le fichier dans le dépôt GitHub. Le site est à jour en une à deux minutes.
- **Automatique** : section « Publier automatiquement sur GitHub ». Créez un jeton d'accès personnel GitHub (Settings > Developer settings > Fine-grained tokens) limité à ce dépôt avec la permission « Contents : read and write », collez-le dans le formulaire, puis « Publier sur GitHub ».

Le bouton « Enregistrer le brouillon » garde vos modifications dans le navigateur sans les publier.

## À savoir sur la sécurité

Le code d'accès est vérifié dans le navigateur : il dissuade un visiteur curieux mais ne constitue pas une authentification serveur, car un site GitHub Pages est statique. Ne stockez rien de confidentiel dans cet écran, et si vous utilisez la publication automatique, ne laissez pas le jeton enregistré sur un ordinateur partagé (décochez « Retenir ces paramètres »).

Pour une vraie protection, il faudrait un hébergement avec backend (Netlify Identity, Cloudflare Access ou un petit serveur).
