---
marp: false
size: 4:3
style: |
  h2, h3, p {
    font-size: 20px;
  }
  li {
    font-size:20px
  }
headingDivider: 1
header: 
paginate: 
footer: Licence 2 Informatique &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ISI (Institut Supérieur D'Informatique) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; RD
---
<img src="../isi.png" alt="ISI" width="100px">


# **PROJET — TECHNOLOGIE WEB**
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

<img src="../html.jpeg" alt="html" width="100px">
<img src="css-3.webp" alt="html" width="100px">

---

**HTML5 & CSS3 uniquement — Durée : 1 semaine**

---

## INFORMATIONS IMPORTANTES


**Date limite de rendu :** 30/03/26 + **PRÉSENTATION**

**Nature du projet :** Projet individuel

**Technologie autorisée :** HTML5 et CSS3 **uniquement** — Pas de JavaScript, pas de Bootstrap, pas de framework, pas de variables

---

## CONTEXTE DU PROJET

La restauration est un secteur en pleine transformation numérique. Aujourd'hui, **90 % des clients recherchent un restaurant en ligne avant de se déplacer**. Un site vitrine soigné est devenu indispensable pour tout établissement qui souhaite attirer et fidéliser sa clientèle.

Vous êtes chargé(e) de concevoir et développer le **site vitrine complet** d'un restaurant-traiteur fictif africain nommé **« SaveursD'Afrique »**, spécialisé dans la cuisine africaine moderne et les prestations traiteur pour événements (mariages, baptêmes, séminaires d'entreprise).

Le site doit être **élégant, appétissant et professionnel**, en s'appuyant uniquement sur HTML5 et CSS3.

---

## SITES DE RÉFÉRENCE ET D'INSPIRATION

Avant de commencer, **prenez 30 minutes** pour visiter ces sites et analyser leur design, leur mise en page et leur typographie. Notez ce qui vous inspire pour votre projet.

### Sites de restaurants à observer

| Site | Lien | Ce qu'on y apprend |
|---|---|---|
| **Noma (Copenhague)** | https://noma.dk | Hero pleine page, typographie minimaliste, narration visuelle |
| **Paul Bocuse** | https://www.bocuse.fr | Élégance, mise en avant du chef, hiérarchie de l'information |
| **Tacos de Lyon** | https://tacosdelyon.sn/ |design moderne, structure simple |
| **Gucci Osteria** | https://www.gucciosteria.com | Identité forte, photos immersives, navigation épurée |
| **Sunday in Brooklyn** | https://www.sundayinbrooklyn.com | Ambiance, couleurs chaudes, typographie expressive |

### Galeries d'inspiration design web

| Plateforme | Lien | Comment l'utiliser |
|---|---|---|
| **Awwwards — Food & Drink** | https://www.awwwards.com/websites/food-drink/ | Meilleurs sites du secteur récompensés par des designers |
| **Awwwards — Restaurant** | https://www.awwwards.com/tasty-design-restaurant-and-catering-websites.html | Sélection de 40 sites restaurant/traiteur analysés |
| **Awwwards — Hôtel & Restaurant** | https://www.awwwards.com/websites/hotel-restaurant/ | Designs hôtellerie-restauration haut de gamme |
| **99designs — Restaurant** | https://99designs.com/inspiration/websites/restaurant | 100+ exemples variés, du classique au moderne |
| **Dribbble** | https://dribbble.com/search/restaurant-website | Maquettes UI/UX de pages restaurant |
| **Behance** | https://www.behance.net/search/projects?search=restaurant+website | Projets complets avec processus de design |
| **Webdesign Inspiration** | https://www.webdesign-inspiration.com/fr/webdesign/industrie/restaurant | Galerie classée par industrie |

### Articles techniques utiles

| Article | Lien |
|---|---|
| Guide complet site restaurant 2026 | https://www.gotrayful.com/fr/blog/guide-complet-site-web-restaurant-2026 |
| 10 exemples à s'inspirer | https://www.klixi.io/fr/blog/site-internet-restaurant-10-exemples-de-sites-web-pour-s-inspirer-5976 |
| Top 30 meilleurs sites restaurant | https://www.elias.studio/blog/post/les-30-meilleurs-site-internet-de-restaurant |
| Top 10 sites restaurant 2025 | https://agencegalopins.com/site-web/10-meilleurs-sites-internet-restaurant/ |

> 💡 **Conseil :** Sur chaque site que vous visitez, ouvrez les **DevTools** (F12 → Inspecteur) pour observer les couleurs, les polices et les propriétés CSS utilisées. C'est votre meilleure école.

---

## PAGES OBLIGATOIRES

Le site doit comporter **3 pages HTML** liées par une navigation cohérente.

---

### PAGE 1 — `index.html` (Accueil)

#### Section HEADER / NAVIGATION
- Logo textuel ou image du restaurant « SaveursD'Afrique »
- Barre de navigation horizontale avec les 3 liens : **Accueil**, **Notre Carte**, **Contact**
- La navigation doit être **fixe en haut** de la page (`position: fixed`)
- Un style visuel clair : fond sombre ou couleur de marque, texte lisible

#### Section HERO
- Image de fond pleine largeur (photo de plat ou d'ambiance — depuis Unsplash ou Pexels)
- Titre principal `<h1>` : « La cuisine africaine moderne, livrée chez vous »
- Sous-titre `<h2>` court et accrocheur
- Deux boutons CTA côte à côte : **« Voir notre carte »** et **« Demander un devis traiteur »**
- Un **overlay sombre** semi-transparent sur l'image pour garantir la lisibilité du texte

#### Section « NOTRE HISTOIRE »
- Disposition en deux colonnes : **texte à gauche**, **image à droite** (Flexbox)
- Texte fictif de 3 à 5 lignes présentant l'histoire du restaurant et la philosophie du chef
- Image du chef ou de la cuisine

#### Section « NOS SPÉCIALITÉS »
- Grille de **4 plats signature** en **CSS Grid** (2 colonnes × 2 lignes)
- Chaque carte de plat contient : photo du plat, nom du plat, courte description (2 lignes), prix fictif
- Effet de survol (`hover`) : légère ombre portée et remontée de la carte (`transform: translateY`)

#### Section « NOS PRESTATIONS TRAITEUR »
- 3 prestations présentées en **Flexbox** : Mariages, Événements d'entreprise, Baptêmes & Cérémonies
- Chaque prestation : icône (emoji ou caractère Unicode), titre, description courte (2-3 lignes)

#### Section CTA TRAITEUR
- Bandeau pleine largeur avec fond coloré (couleur d'accent de votre palette)
- Texte percutant : « Vous organisez un événement ? Faites confiance à SaveursD'Afrique »
- Bouton lien vers `contact.html`

#### FOOTER
- 3 colonnes en Flexbox : **À propos** (description courte), **Navigation** (liens), **Contact** (adresse fictive, téléphone, email)
- Ligne de copyright : `© 2026 SaveursD'Afrique — Tous droits réservés`

---

### PAGE 2 — `carte.html` (Notre Carte)

#### Section HERO INTERNE
- Bannière pleine largeur (image différente de l'accueil)
- Titre de la page : « Notre Carte »
- Fil d'Ariane simple : `Accueil > Notre Carte`

#### Section ENTRÉES
- Titre de section `<h2>` avec décoration CSS (ligne sous le titre, couleur d'accent)
- Grille de **4 entrées** en CSS Grid (2 colonnes sur desktop, 1 sur mobile)
- Chaque plat : nom, description courte, prix fictif

#### Section PLATS PRINCIPAUX
- Même mise en page que les entrées, **6 plats principaux**
- Alternance visuelle possible (fond légèrement différent pour distinguer les sections)

#### Section DESSERTS
- Même mise en page, **3 desserts**

#### Section FORMULES TRAITEUR
- Tableau HTML `<table>` présentant les formules événementielles :
  - Colonnes : Formule, Nombre de personnes, Prix par personne, Inclus
  - 3 formules : Essentielle, Prestige, Premium
  - Styles CSS appliqués au tableau (alternance des lignes, bordures, en-tête coloré)

---

### PAGE 3 — `contact.html` (Contact & Réservation)

#### Section HERO INTERNE
- Bannière pleine largeur
- Titre : « Contactez-nous »
- Fil d'Ariane : `Accueil > Contact`

#### Section FORMULAIRE DE CONTACT
- Disposition en deux colonnes (Flexbox) : **formulaire à gauche**, **informations à droite**
- Le formulaire contient les champs HTML suivants (sans validation JavaScript) :
  - Nom complet (`<input type="text">`)
  - Email (`<input type="email">`)
  - Téléphone (`<input type="tel">`)
  - Type de demande (`<select>` : Réservation table / Devis traiteur / Autre)
  - Date de l'événement (`<input type="date">`)
  - Nombre de personnes (`<input type="number">`)
  - Message (`<textarea>`)
  - Bouton d'envoi stylisé
- Les champs doivent être stylisés en CSS (bordures, focus coloré, padding, coins arrondis)

#### Informations à droite du formulaire
- Adresse fictive avec icône (emoji)
- Numéro de téléphone fictif
- Email fictif
- Horaires d'ouverture présentés dans un tableau ou une liste stylisée

#### Section CARTE
- `<iframe>` Google Maps intégré (n'importe quel lieu fictif ou réel de Dakar)

---

## CONTRAINTES TECHNIQUES

### OBLIGATOIRE

- **HTML5 sémantique uniquement** : `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`
- **CSS externe uniquement** : un seul fichier `style.css`. **Aucun CSS inline** dans le HTML

- **Flexbox** utilisé pour au moins 2 mises en page (navbar, footer, colonnes)
- **CSS Grid** utilisé pour au moins 1 mise en page (grille de plats)
- **Google Fonts** : au minimum 2 polices (une pour les titres, une pour le corps de texte)
- **Attribut `alt`** renseigné sur toutes les images
- **Palette de couleurs** : maximum 4 couleurs, cohérentes avec l'identité africaine moderne
- **Commentaires CSS** : chaque section du CSS doit être commentée (`/* === NAVBAR === */`)

### INTERDIT

- JavaScript (même une seule ligne)
- Bootstrap ou tout autre framework CSS
- CSS inline dans les fichiers HTML
- Templates ou thèmes existants
- Générateurs de code automatiques

---

## ARBORESCENCE DU PROJET

```
NOM-Prenom-SaveursAfrique/
├── index.html
├── carte.html
├── contact.html
├── css/
│   └── style.css
├── images/
│   └── (vos photos depuis Unsplash/Pexels)
└── README.md
```

---

## SUGGESTIONS DE PALETTE DE COULEURS

Voici trois palettes adaptées à un restaurant africain moderne. Choisissez-en une ou créez la vôtre sur **https://coolors.co**.

### Palette 1 — Chaleur & Terre
| Rôle | Couleur | Code hex |
|---|---|---|
| Principale | Terre de sienne | `#8B4513` |
| Accent | Or chaud | `#D4A017` |
| Fond clair | Sable | `#FDF5E6` |
| Texte | Brun foncé | `#2C1810` |

### Palette 2 — Moderne & Épuré
| Rôle | Couleur | Code hex |
|---|---|---|
| Principale | Vert forêt | `#2D5016` |
| Accent | Orange vif | `#E8621A` |
| Fond clair | Blanc cassé | `#FAFAF7` |
| Texte | Anthracite | `#1A1A1A` |

### Palette 3 — Nuit & Luxe
| Rôle | Couleur | Code hex |
|---|---|---|
| Principale | Noir profond | `#0D0D0D` |
| Accent | Or | `#C9A84C` |
| Fond clair | Crème | `#F5F0E8` |
| Texte | Gris clair | `#E8E8E8` |

---

## SUGGESTIONS DE POLICES GOOGLE FONTS

Visitez **https://fonts.google.com** et choisissez parmi ces combinaisons recommandées :

| Titres | Corps | Style rendu |
|---|---|---|
| **Playfair Display** | **Lato** | Élégant, gastronomique |
| **Cormorant Garamond** | **Montserrat** | Luxe, raffiné |
| **Josefin Sans** | **Open Sans** | Moderne, minimaliste |
| **Libre Baskerville** | **Source Sans 3** | Traditionnel, chaleureux |

---

## IMAGES LIBRES DE DROITS

Utilisez ces sources pour trouver vos photos de plats, d'ambiance et de chefs :

| Source | Lien | Conseil de recherche |
|---|---|---|
| **Unsplash** | https://unsplash.com | Rechercher : « african food », « restaurant interior », « chef cooking » |
| **Pexels** | https://www.pexels.com/fr-fr/ | Rechercher : « cuisine africaine », « food photography », « catering » |

---

## CRITÈRES D'ÉVALUATION

| Critère | Points | Détails |
|---|---|---|
| **Structure HTML** | /5 | Balises sémantiques correctes, hiérarchie H1→H6 logique, `alt` sur toutes les images, 3 pages liées |
| **CSS — Mise en page** | /5 | Flexbox et CSS Grid utilisés correctement, navbar fixe, disposition en colonnes, grille de plats |
| **CSS — Design visuel** | /3 | Cohérence de la palette , typographie (Google Fonts), effets hover, esthétique générale |
| **Formulaire HTML** | /2 | Tous les champs présents, types corrects (`email`, `tel`, `date`, `select`, `textarea`, `...`), stylisé en CSS |
| **Qualité du code** | /2 | Indentation propre, commentaires CSS, organisation des fichiers, aucun CSS inline |
| **Tableau et /ou iframe** | /1 | Tableau des formules traiteur stylisé, iframe Google Maps intégré |
| **TOTAL** | **/20** | |

---

## CONSEILS PRATIQUES

1. **Commencez par le design sur papier.** Avant d'écrire une seule ligne de code, esquissez vos 3 pages sur une feuille. Où va la navbar ? Le hero ? La grille ?
2. **Structure d'abord.** Rédigez tout le HTML d'une page avant d'ouvrir `style.css`.
3. **Une section à la fois.** Stylez section par section, pas tout en même temps.
4. **Testez souvent.** Ouvrez votre fichier dans le navigateur après chaque modification significative.
5. **Validez votre HTML.** Utilisez **https://validator.w3.org** avant de rendre.
6. **Inspectez les sites de référence.** F12 sur les sites donnés en exemple est votre meilleur cours de CSS.

---

**Montrez-nous votre sens du design et votre rigueur technique. Un beau site, c'est d'abord un HTML propre et un CSS bien organisé.**

**Bon courage !**

