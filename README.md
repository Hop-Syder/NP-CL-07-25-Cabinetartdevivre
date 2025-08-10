# Cabinet ART DE VIVRE — Site web

Site vitrine statique pour le cabinet de psychologie ART DE VIVRE. Le projet est composé de pages HTML, de ressources front (CSS/JS/Images) et de deux formulaires (contact et prise de rendez-vous) côté serveur en PHP.

## Aperçu
- **Type de projet**: site statique + formulaires PHP
- **Technos**: HTML5, CSS3, JavaScript, Bootstrap 5, AOS, Swiper, GLightbox
- **Formulaires**: `forms/contact.php`, `forms/appointment.php` (requièrent une petite librairie PHP non incluse par défaut)

## Arborescence
```
.
├─ 404.html
├─ about.html
├─ appointment.html
├─ blog.html
├─ contact.html
├─ index.html
├─ services.html
├─ assets/
│  ├─ css/
│  │  └─ main.css
│  ├─ img/
│  ├─ js/
│  │  └─ main.js
│  ├─ scss/
│  │  └─ Readme.txt
│  └─ vendor/
│     ├─ bootstrap/
│     ├─ bootstrap-icons/
│     ├─ fontawesome-free/
│     ├─ aos/
│     ├─ swiper/
│     ├─ glightbox/
│     ├─ imagesloaded/
│     ├─ isotope-layout/
│     └─ php-email-form/   ← répertoire présent, fichier principal non fourni
└─ forms/
   ├─ contact.php
   ├─ appointment.php
   └─ Readme.txt
```

## Prérequis
- Pour consulter le site: un simple serveur HTTP (ou ouvrir les fichiers HTML dans un navigateur; note: certaines fonctionnalités comme AOS nécessitent un contexte HTTP pour charger correctement les assets).

## Lancer en local
- Option 1 — uniquement statique (sans PHP):
  ```bash
  # À la racine du projet
  python3 -m http.server 8000
  # Ouvrir http://localhost:8000
  ```
  Les formulaires ne fonctionneront pas (appel PHP requis).

- Option 2 — avec PHP (recommandé pour tester les formulaires):
  ```bash
  # À la racine du projet
  php -S localhost:8000 -t .
  # Ouvrir http://localhost:8000
  ```


## Points SEO/Analytics à personnaliser
Présents dans `index.html` (et à répliquer si besoin dans d’autres pages):
- Balises `<meta name="description">`, `<meta name="keywords">`.
- Données structurées JSON-LD (nom, coordonnées, réseaux sociaux, géolocalisation).
- Balises Open Graph (titre, description, image, URL).
- Google Tag Manager/Analytics: remplacer l’ID de conteneur `GTM-NN2KF45P` par votre propre ID.
- Vérifications Search Console/Bing/Yandex: remplacer les codes de vérification.
- Politique de confidentialité/CGU: mettre à jour les URL dans les metas.
- En-tête CSP actuel très strict: si vous utilisez GTM/Google Fonts/ressources externes supplémentaires, adaptez la directive `Content-Security-Policy` pour autoriser les domaines requis.


## Personnalisation UI
- CSS principal: `assets/css/main.css`.
- JS principal: `assets/js/main.js`.
- Bibliothèques UI: `assets/vendor/*` (Bootstrap, AOS, Swiper, GLightbox...).
- Images: `assets/img/`.
- Le dossier `assets/scss/` ne contient ici qu’un Readme; si vous souhaitez une chaîne de compilation SCSS → CSS, ajoutez votre configuration (Sass/Node, etc.) ou travaillez directement dans `main.css`.

## Tests rapides
- Navigation: ouvrir `index.html`, vérifier les liens vers `about.html`, `services.html`, `contact.html`, `appointment.html`.
- Formulaires (avec serveur PHP actif): soumettre un test et vérifier la réponse (200/OK) et la réception d’email.
- Console navigateur: vérifier l’absence d’erreurs JS et de ressources bloquées par la CSP.

## Crédits et licence
- Le code front s’appuie sur des bibliothèques tierces (Bootstrap, AOS, Swiper, GLightbox, etc.) — se référer à leurs licences respectives.
- Les fichiers  et `forms/Readme.txt` mentionnent une dépendance au composant « PHP Email Form » associé à une version pro de template BootstrapMade. Respecter les conditions de licence/attribution le cas échéant.


