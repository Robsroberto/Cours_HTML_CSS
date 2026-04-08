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


---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ
# Cours 3 : Les Listes en HTML

## Objectif du Cours

Comprendre l'utilisation des listes en HTML pour structurer et organiser le contenu des pages web. Ce cours couvrira les trois types de listes HTML : ordonnée, non ordonnée et liste de définition.

## Introduction

Les listes sont un élément essentiel pour organiser l'information sur une page web. HTML propose trois types principaux de listes, chacune adaptée à des contextes spécifiques.

## 1. Liste Non Ordonnée `<ul>` (Unordered List)

La liste non ordonnée est utilisée lorsque l'ordre des éléments n'a pas d'importance. Les éléments sont généralement affichés avec des puces.

### Exemple :

```html
<ul>
  <li>Pommes</li>
  <li>Oranges</li>
  <li>Bananes</li>
</ul>
```

- Pommes
- Oranges
- Bananes

#### Attributs Possibles :

- `type`: Définit le type de puce utilisé. Les valeurs courantes sont `disc`, `circle`, et `square`.

```html
<ul type="circle">
  <li>Élément 1</li>
  <li>Élément 2</li>
</ul>
```

Vous avez raison, j'ai omis de mentionner l'attribut `start` pour la balise `<ol>`. Cet attribut permet de spécifier la valeur de départ de la numérotation. Voici une mise à jour de la section pertinente :

## 2. Liste Ordonnée `<ol>` (Ordered List)

La liste ordonnée est utilisée lorsque l'ordre des éléments a de l'importance. Les éléments sont numérotés par défaut.

### Exemple :

```html
<ol>
  <li>Introduction</li>
  <li>Développement</li>
  <li>Conclusion</li>
</ol>
```

1. Introduction
2. Développement
3. Conclusion

#### Attributs Possibles :

- `type`: Définit le type de numérotation. Les valeurs courantes sont `1` (numérotation), `A`, `a`, `I`, `i`.

```html
<ol type="A">
  <li>Étape 1</li>
  <li>Étape 2</li>
</ol>

```

- `start`: Spécifie la valeur à partir de laquelle la numérotation commence.

```html
<ol start="5">
  <li>Étape 5</li>
  <li>Étape 6</li>
</ol>
```

Cet exemple commencera la numérotation à partir de 5, donnant comme résultat :

5. Étape 5
6. Étape 6

## 3. Liste de Définition `<dl>` (Definition List)

La liste de définition est utilisée pour définir des termes. Chaque terme est suivi de sa définition.

### Exemple :

```html
<dl>
  <dt>HTML</dt>
  <dd>Langage de balisage pour la création de pages web.</dd>
  <dt>CSS</dt>
  <dd>Langage de style pour la présentation des pages web.</dd>
</dl>
```

 **HTML** 
 
    Langage de balisage pour la création de pages web.

**CSS**

    Langage de style pour la présentation des pages web.

#### Attributs Possibles :

Aucun attribut spécifique aux listes de définition n'est couramment utilisé.

## Imbrication de Listes

Il est possible d'imbriquer des listes à l'intérieur d'autres listes pour créer une structure plus complexe.

### Exemple :

```html
<ul>
  <li>Fruits
    <ul>
      <li>Pommes</li>
      <li>Oranges</li>
    </ul>
  </li>
  <li>Légumes
    <ul>
      <li>Carottes</li>
      <li>Pommes de terre</li>
    </ul>
  </li>
</ul>
```

- Fruits
  - Pommes
  - Oranges
- Légumes
  - Carottes
  - Pommes de terre

En résolvant l'imbrication de la liste, commencez par le niveau le plus élevé et descendez jusqu'au niveau le plus bas.

## Conclusion

Les listes en HTML sont un outil puissant pour organiser et structurer le contenu d'une page web. En comprenant les trois types de listes et leurs attributs, vous serez en mesure d'améliorer la lisibilité et la navigation sur vos pages. Dans le prochain cours, nous explorerons d'autres éléments clés d'HTML pour enrichir davantage la structure de nos documents web.