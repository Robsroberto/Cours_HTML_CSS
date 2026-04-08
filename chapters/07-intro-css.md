# Introduction au CSS

Intro CSS.md 2023-12-26

Cours 4 : Introduction au CSS
Objectif du Cours
Comprendre le rôle du CSS (Cascading Style Sheets) dans la conception web, ses différentes méthodes
d'intégration, et explorer la syntaxe de base pour styliser des pages HTML. Ce cours introduira également
SASS et SCSS comme extensions de CSS.
Introduction
Le CSS est un langage de style utilisé pour définir la présentation d'un document HTML. Il permet de contrôler
la mise en forme, le positionnement et l'apparence visuelle des éléments sur une page web.
Pourquoi Utiliser le CSS ?
Séparation des Responsabilités : Le CSS permet de séparer la structure (HTML) du style (CSS),
facilitant la maintenance et la mise à jour du code.
Consistance : Appliquer un ensemble cohérent de styles à travers un site, assurant une apparence
uniforme.
Adaptabilité : Permet d'ajuster l'apparence d'un site pour différents types d'appareils (responsive
design).
Syntaxe de Base CSS
La syntaxe CSS de base suit le modèle:
selecteur {
propriete: valeur(s);
...
propriete n : valeur(s)
}
Exemple :
body {
font-family: 'Helvetica', sans-serif;
1 / 4

Intro CSS.md 2023-12-26
background-color: red;
color: white;
}
h1 {
font-size: 24px;
color: yellow;
}
Types de Sélecteurs
Les sélecteurs CSS déterminent quels éléments dans le document seront stylisés.
Sélecteur d'Élément html : Sélectionne tous les éléments du type spécifié.
p {
font-size: 16px;
}
Sélecteur de Classe : Sélectionne tous les éléments avec la classe spécifiée.
.important {
font-weight: bold;
}
Sélecteur d'ID : Sélectionne un élément avec l'ID spécifié.
#header {
background-color: black;
color: white;
}
SASS et SCSS
SASS (Syntactically Awesome Stylesheets) et SCSS (Sassy CSS) sont des préprocesseurs CSS qui ajoutent des
fonctionnalités supplémentaires comme les variables, les mixins, et les imports.
SASS : Utilise une syntaxe indentée sans accolades ni points-virgules.
$couleurPrincipale: #3498db
body
background-color: $couleurPrincipale
2 / 4

Intro CSS.md 2023-12-26
SCSS : Utilise une syntaxe similaire à CSS avec des extensions.
$couleurPrincipale: #3498db;
body {
background-color: $couleurPrincipale;
}
Méthodes d'Intégration du CSS
Il existe trois principales méthodes pour intégrer du CSS dans une page HTML.
1. Balise <style>
Utiliser la balise <style> dans l'en-tête HTML pour incorporer du CSS directement dans le document.
<!DOCTYPE html>
<html lang="fr">
<head>
<style>
body {
font-family: 'Arial', sans-serif;
}
</style>
</head>
<body>
<!-- Contenu de la page -->
</body>
</html>
2. Attribut style
Utiliser l'attribut style directement dans les balises HTML pour appliquer des styles à des éléments
spécifiques.
<p style="color: #ff0000; font-size: 16px;">Texte Rouge</p>
3. Fichier Externe avec la Balise <link>
Créer un fichier CSS externe et l'associer à la page HTML à l'aide de la balise <link>.
Fichier CSS (style.css)
body {
background-color: brown;
3 / 4

Intro CSS.md 2023-12-26
color: grey;
}
Page HTML
<!DOCTYPE html>
<html lang="fr">
<head>
<link rel="stylesheet" href="style.css">
</head>
<body>
<!-- Contenu de la page -->
</body>
</html>
Quelques Propriétés Courantes
color : Définit la couleur du texte.
font-size : Définit la taille de la police.
font-family : Définit la police de caractères.
background-color : Définit la couleur de fond.
margin et padding : Contrôlent les marges et les espacements internes.
Conclusion
Ce cours a introduit les bases du CSS, son utilité, et les différentes méthodes pour l'intégrer dans une page
web. En comprenant la syntaxe de base et les types de sélecteurs, vous serez prêt à styliser vos pages HTML
de manière plus avancée. Dans les cours suivants, nous explorerons des fonctionnalités plus avancées de CSS.
4 / 4


---

## Exercices pratiques

> Mets en pratique ce que tu viens d'apprendre avant de passer au chapitre suivant.

### Exercice 1 — Application directe

Applique les notions vues sur un exemple concret de ton choix.

**Consigne :** Réalise l'exercice correspondant à ce chapitre et valide ta compréhension avant de continuer.

### Exercice 2 — Questions de compréhension

1. Quel est le concept fondamental de ce chapitre ?
2. Cite un cas d'usage concret en contexte professionnel.
3. Quelle notion t'a semblé la plus complexe ? Comment l'as-tu abordée ?

### Checklist avant de continuer

- [ ] J'ai lu et compris le contenu du chapitre
- [ ] J'ai réalisé au moins un exercice pratique
- [ ] Je peux résumer ce chapitre en 3 points essentiels
