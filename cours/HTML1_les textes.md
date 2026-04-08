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

# Cours 1 : Structuration de Document Web avec HTML - Balises de Texte

## Objectif du Cours

Comprendre les bases de la structuration de documents web en utilisant HTML. Ce cours se concentrera sur les balises de texte pour créer du contenu structuré.

## Introduction

HTML (HyperText Markup Language) est le langage standard utilisé pour créer et structurer le contenu des pages web. Il utilise une syntaxe de balisage pour définir la structure d'une page. Dans ce cours, nous explorerons les balises de texte essentielles pour formater et organiser le contenu de manière lisible, tout en examinant leur rôle dans le référencement.

### Structure de Base d'une Page HTML

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titre de la Page</title>
</head>
<body>

<!-- Contenu de la page -->

</body>
</html>
```

- `<!DOCTYPE html>` : Indique la version HTML (HTML5) du document.
- `<html lang="fr">` : Déclare la langue du document (en français dans cet exemple).
- `<head>` : Contient des méta-informations sur le document.
- `<meta charset="UTF-8">` : Spécifie l'encodage des caractères.
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">` : Ajuste l'affichage sur différents appareils.
- `<title>` : Définit le titre de la page, affiché dans l'onglet du navigateur.
- `<body>` : Contient le contenu visible de la page.

## 1. Paragraphe - `<p>` (Paragraphe)

La balise `<p>` est utilisée pour définir des paragraphes de texte. Elle crée un espace vertical avant et après le texte.

Exemple :
```html
<p>Ceci est un paragraphe de texte.</p>
<p>Voici un autre paragraphe.</p>
```

## 2. En-têtes - `<h1>` à `<h6>` (Titres et Sous-Titres)

Les balises `<h1>` à `<h6>` sont utilisées pour définir les titres et sous-titres. `<h1>` est le titre principal, `<h2>` est un sous-titre, et ainsi de suite.

Exemple :
```html
<h1>Titre Principal</h1>
<h2>Sous-Titre</h2>
<h3>Sous-Sous-Titre</h3>
```

## 3. Mise en Forme - `<strong>`, `<em>`, `<u>` (Gras, Italique, Souligné)

- `<strong>` : Texte en **gras**. Indique une importance forte.
- `<em>` : Texte en *italique*. Indique une emphase.
- `<u>` : Texte souligné. **Non recommandé** pour le style, utilisé plutôt pour les liens.

Exemple :
```html
<p><strong>Texte en gras</strong></p>
<p><em>Texte en italique</em></p>
<p><u>Texte souligné</u></p>
```

## 4. Saut de Ligne - `<br>` (Break)

La balise `<br>` est utilisée pour insérer un saut de ligne à l'intérieur d'un texte.

Exemple :
```html
<p>Ceci est une ligne.<br>Et voici une nouvelle ligne.</p>
```

## 5. Ligne Horizontale - `<hr>` (Horizontal Rule)

La balise `<hr>` crée une ligne horizontale pour diviser le contenu.

Exemple :
```html
<p>Ceci est un paragraphe.</p>
<hr>
<p>Et voici un autre paragraphe.</p>
```

## 6. Commentaires - `<!-- ... -->`

Les commentaires sont utilisés pour ajouter des annotations dans le code HTML. Ils ne sont pas affichés dans la page web.

Exemple :
```html
<!-- Ceci est un commentaire -->
<p>Ceci est un paragraphe de texte.</p>
```

## 7. Balises de Formatage Additionnelles

### `<big>` et `<small>` (Texte plus Grand ou plus Petit)

- `<big>` : Augmente la taille du texte.
- `<small>` : Réduit la taille du texte.

Exemple :
```html
<p><big>Ce texte est plus grand.</big></p>
<p><small>Ce texte est plus petit.</small></p>
```

### `<code>` (Code Informatique)

La balise `<code>` est utilisée pour représenter du code informatique.

Exemple :
```html
<p>Utilisez la commande <code>git commit</code> pour valider les changements.</p>
```

### `<blockquote>` (Citation Longue)

La balise `<blockquote>` est utilisée pour les citations longues qui peuvent s'étendre sur plusieurs lignes.

Exemple :
```html
<blockquote>
  <p>La vie est vraiment simple, mais nous insistons à la rendre compliquée.</p>
  <footer>Confucius</footer>
</blockquote>
```

### `<q>` et `<cite>` (Citation Courte et Source)

- `<q>` : Indique une citation courte.
- `<cite>` : Indique la source de la citation.

Exemple :
```html
<p><q>La simplicité est la sophistication ultime.</q></p>
<cite>Leonardo da Vinci</cite>
```

### `<s>`, `<ins>`, `<del>` (Texte Barré, Souligné, Barré)

- `<s>` : Indique du texte barré. **Peut indiquer une suppression non recommandée pour le référencement.**
- `<ins>` : Indique du texte souligné. **Peut indiquer une insertion.**
- `<del>` : Indique du texte barré avec une ligne en travers. **Peut indiquer une suppression.**

Exemple :
```html
<p><s>Ce texte est barré.</s></p>
<p><ins>Ce texte est souligné.</ins></p>
<p><del>Ce texte est barré avec une ligne en travers.</del></p>
```

### `<sup>` et `<sub>` (Exposant et Indice)

- `<sup>`

 : Utilisé pour le texte en exposant.
- `<sub>` : Utilisé pour le texte en indice.

Exemple :
```html
<p>E=mc<sup>2</sup></p>
<p>H<sub>2</sub>O</p>
```

### `<mark>` (Mise en Évidence)

La balise `<mark>` est utilisée pour mettre en évidence une partie de texte.

Exemple :
```html
<p>Cette information est <mark>importante</mark>.</p>
```

### `<u>` (Souligné)

La balise `<u>` est utilisée pour indiquer du texte souligné.

Exemple :
```html
<p><u>Ce texte est souligné.</u></p>
```

## Balises de Type Bloc vs Balises de Type En Ligne

Les balises de type bloc définissent des blocs de contenu et créent une nouvelle ligne avant et après le contenu. Exemples : `<p>`, `<h1>`, `<div>`.

Les balises de type ligne n'affectent pas la structure globale de la page et ne créent pas de nouvelle ligne. Exemples : `<strong>`, `<em>`, `<a>`...

## Conclusion

Ce cours a exploré diverses balises de texte HTML pour formater et organiser le contenu des pages web. Pratiquez l'utilisation de ces balises pour maîtriser la création de documents structurés. Dans les cours suivants, nous aborderons d'autres aspects passionnants du développement web.