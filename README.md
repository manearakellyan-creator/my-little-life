# MY LITTLE LIFE — guide de démarrage

## Ce que contient cette première version
- Accueil quotidien, tâches, priorités, catégories et rendez-vous.
- Planning par jour avec sélection des jours de la semaine.
- Espace études : matières, dates d'examen, chapitres et génération d'un programme de révision.
- Habitudes, objectifs avec progression, notes.
- Menus hebdomadaires équilibrés d'inspiration économique, liste de courses et budget.
- Statistiques simples, bilan hebdomadaire, conseils pour débloquer une séance de révision.
- Sauvegarde JSON et restauration.
- Export du planning au format `.ics` importable dans Apple Calendar.
- PWA avec manifeste et service worker pour l'installation et une utilisation hors ligne après le premier chargement.

## Hébergement gratuit avec GitHub Pages
1. Sur un ordinateur, crée un compte sur https://github.com si tu n'en as pas.
2. Crée un nouveau dépôt, par exemple `my-little-life`. Choisis **Public**.
3. Décompresse le ZIP et envoie tous les fichiers du dossier dans le dépôt (bouton **Add file → Upload files**).
4. Va dans **Settings → Pages**.
5. Dans **Build and deployment**, choisis **Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**.
6. Attends la publication. GitHub Pages affiche une adresse du type `https://TON-PSEUDO.github.io/my-little-life/`.
7. Ouvre cette adresse dans Safari sur ton iPhone.

## Installation sur iPhone
1. Ouvre le lien hébergé dans **Safari** (pas dans un navigateur intégré à une autre application).
2. Appuie sur le bouton **Partager** (carré avec flèche vers le haut).
3. Fais défiler et choisis **Sur l’écran d’accueil**.
4. Vérifie le nom « My Little Life », active si proposé l'option d'ouverture comme app web, puis touche **Ajouter**.
5. L'icône apparaît sur l'écran d'accueil.

## Données, sauvegarde et appareils
Les données sont stockées dans le stockage local du navigateur (`localStorage`) sur l'appareil utilisé. Elles ne sont pas envoyées vers un serveur. Utilise régulièrement **Bilan → Exporter mes données** et conserve le fichier JSON dans Fichiers/iCloud Drive. Pour restaurer, ouvre l'application sur l'appareil cible et choisis **Restaurer**.
Cette version ne synchronise pas automatiquement les données entre iPhone, iPad et ordinateur. Pour une synchronisation multi-appareils fiable, il faudra ajouter une base de données distante avec authentification (par exemple Supabase) et une politique de sauvegarde.

## Apple Calendar : possibilité et limite
Dans Planning, le bouton **Exporter vers Apple Calendar (.ics)** crée un fichier calendrier. Sur iPhone, ouvre le fichier et ajoute les événements à Calendrier. C'est un export ponctuel à sens unique : les modifications ultérieures dans MY LITTLE LIFE ne se répercutent pas automatiquement dans Apple Calendar, et inversement. Une synchronisation bidirectionnelle demanderait une intégration serveur/API et des autorisations supplémentaires ; une PWA web seule ne dispose pas d'un accès complet à la base privée d'Apple Calendar.

## Personnalisation à terminer
Les menus et exemples sont des suggestions de départ. Ajoute tes matières, chapitres, dates d'examen, préférences alimentaires et recettes favorites pour personnaliser ton espace. Les menus proposés sont des idées générales, pas un avis nutritionnel personnalisé.

## Sécurité et limites
- Le site doit être hébergé en HTTPS pour que le service worker et l'installation PWA fonctionnent correctement.
- Les données sont locales : effacer les données du navigateur ou désinstaller/effacer le site peut les supprimer. Exporte des sauvegardes.
- Le cache hors ligne conserve les fichiers de l'application, mais les polices Google peuvent nécessiter une connexion lors du premier affichage.
- Le ZIP est un site statique prêt à héberger ; il n'est pas encore publié en ligne.
