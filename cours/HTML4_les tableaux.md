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

# Cours 4 : Les Tableaux en HTML
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ


---



## Introduction aux Tableaux en HTML

Les tableaux en HTML sont utilisés pour organiser et afficher des données de manière structurée. Ils peuvent être simples ou complexes en fonction des besoins. Voyons en détail comment créer et styliser des tableaux.

### Tableau Simple

Un tableau simple est constitué de lignes et de colonnes de cellules de données. Chaque ligne est défini par l'élément `<tr>` et chaque cellule est définie par l'élément `<td>`.

```html
<table>
    <tr>
        <td>Donnée 1</td>
        <td>Donnée 2</td>
    </tr>
    <tr>
        <td>Donnée 3</td>
        <td>Donnée 4</td>
    </tr>
</table>
```

### Tableau avec En-tête

Les tableaux peuvent avoir une première ligne d'en-têtes définie avec l'élément `<th>`.

```html
<table>
    <tr>
        <th>Titre 1</th>
        <th>Titre 2</th>
    </tr>
    <tr>
        <td>Donnée 1</td>
        <td>Donnée 2</td>
    </tr>
    <tr>
        <td>Donnée 3</td>
        <td>Donnée 4</td>
    </tr>
</table>
```

### Tableau Structuré

Un tableau peut être structuré en utilisant les éléments `<thead>`, `<tbody>`, et `<tfoot>`.

```html
<table>
    <thead>
        <tr>
            <th>Titre 1</th>
            <th>Titre 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Donnée 1</td>
            <td>Donnée 2</td>
        </tr>
        <tr>
            <td>Donnée 3</td>
            <td>Donnée 4</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Total</td>
            <td>100</td>
        </tr>
    </tfoot>
</table>
```

## Styles CSS pour les Tableaux

Améliorons l'apparence de nos tableaux en utilisant des styles CSS.

```css
table {
    width: 100%;
    border-collapse: collapse;
}

th, td {
    border: 1px solid black;
    padding: 8px;
    text-align: left;
}
```

La propriété `border-collapse: collapse` assure que les bordures se fusionnent pour un aspect plus propre.

## Fusion de Colonnes et de Lignes

### Colspan et Rowspan

L'attribut `colspan` permet de fusionner des colonnes, tandis que `rowspan` permet de fusionner des lignes.

```html
<td colspan="2">Colonne Fusionnée</td>
<td rowspan="2">Ligne Fusionnée</td>
```

### Fusion de Colonnes (`colspan`)

Lorsque vous utilisez l'attribut `colspan` sur une cellule d'une ligne, cela signifie que la cellule va s'étendre sur plusieurs colonnes. Voici comment cela fonctionne :

1. **Création du Tableau Complet :** Créez le tableau complet avec toutes les cellules.

    ```html
    <table>
        <tr>
            <td colspan="2">Cellules Fusionnées</td>
            <!-- <td></td> -->
            <td>Ligne 1, Cellule 3</td>
        </tr>
        <tr>
            <td>Ligne 2, Cellule 1</td>
            <td>Ligne 2, Cellule 2</td>
            <td>Ligne 2, Cellule 3</td>
        </tr>
        <tr>
            <td>Ligne 3, Cellule 1</td>
            <td>Ligne 3, Cellule 2</td>
            <td>Ligne 3, Cellule 3</td>
        </tr>
    </table>
    ```

2. **Élimination des Cellules Redondantes :** Retirez les cellules qui ne sont plus nécessaires après la fusion.

    ```html
    <table>
        <tr>
            <td colspan="2">Cellules Fusionnées</td>
            <!-- <td></td> cellule a retirer -->
            <td>Ligne 1, Cellule 3</td>
        </tr>
        <tr>
            <td>Ligne 2, Cellule 1</td>
            <td>Ligne 2, Cellule 2</td>
            <td>Ligne 2, Cellule 3</td>
        </tr>
        <tr>
            <td>Ligne 3, Cellule 1</td>
            <td>Ligne 3, Cellule 2</td>
            <td>Ligne 3, Cellule 3</td>
        </tr>
    </table>
    ```

### Fusion de Lignes (`rowspan`)

Lorsque vous utilisez l'attribut `rowspan` sur une cellule d'une ligne, cela signifie que la cellule va s'étendre sur plusieurs lignes. Voici comment cela fonctionne :

1. **Création du Tableau Complet :** Tout d'abord, créez votre tableau complet avec toutes les cellules, y compris celles qui seront fusionnées.

    ```html
    <table>
        <tr>
            <td rowspan="2">Cellule Fusionnée</td>
            <td>Ligne 1, Cellule 2</td>
            <td>Ligne 1, Cellule 3</td>
        </tr>
        <tr>
            <!-- Cette ligne représente la deuxième ligne -->
            <!-- <td></td> -->
            <td>Ligne 2, Cellule 2</td>
            <td>Ligne 2, Cellule 3</td>
        </tr>
        <tr>
            <td>Ligne 3, Cellule 1</td>
            <td>Ligne 3, Cellule 2</td>
            <td>Ligne 3, Cellule 3</td>
        </tr>
    </table>
    ```

2. **Élimination des Cellules Redondantes :** Une fois le tableau créé, vous pouvez retirer les cellules qui ne sont plus nécessaires après la fusion.

    ```html
    <table>
        <tr>
            <td rowspan="2">Cellule Fusionnée</td>
            <td>Ligne 1, Cellule 2</td>
            <td>Ligne 1, Cellule 3</td>
        </tr>
        
        <tr>
            <!-- <td></td> La deuxième ligne n'a plus besoin de la cellule fusionnée -->
            <td>Ligne 2, Cellule 2</td>
            <td>Ligne 2, Cellule 3</td>
        </tr>
        <tr>
            <td>Ligne 3, Cellule 1</td>
            <td>Ligne 3, Cellule 2</td>
            <td>Ligne 3, Cellule 3</td>
        </tr>
    </table>
    ```


En adoptant cette approche méthodique, vous vous assurez que les fusions sont correctement intégrées dans votre tableau.
### Fusion avec CSS

Parfois, `colspan` et `rowspan` ne suffisent pas. Utilisons du CSS pour personnaliser davantage.

```css
td.colspan_right {
    border-right: none;
}
td.colspan_left {
    border-left: none;
}

td.rowspan {
    border-bottom: none;
}
```

```html
<td class="colspan_right">Donnée Fusionnée</td>
<td class="colspan_left">Donnée Fusionnée</td>
<td class="rowspan">Donnée Fusionnée</td>
```

## Attributs HTML pour les Tableaux

- `<table>` : Conteneur de tableau
- `<tr>` : Ligne de tableau
- `<th>` : En-tête de tableau
- `<td>` : Cellule de données de tableau
- `<thead>` : Section d'en-têtes
- `<tbody>` : Section de corps
- `<tfoot>` : Section de pied de tableau
- `<colspan>` : Fusion de colonnes
- `<rowspan>` : Fusion de lignes
- `<caption>` : Cette balise est utilisée pour ajouter un titre ou une légende à votre tableau.
    - Attributs
        - `align` : Alignement horizontal du titre (top, bottom, left, right).
- `<colgroup>` : Cette balise permet de regrouper des colonnes et de spécifier des propriétés communes pour ces colonnes.
    - Attributs
        - `span` : Nombre de colonnes regroupées.
        - `width` : Largeur des colonnes.
- `<col>` : Utilisée à l'intérieur de `<colgroup>`, cette balise permet de définir les propriétés individuelles des colonnes.
    - Attributs :
        - `span` : Nombre de colonnes regroupées.
        - `width` : Largeur de la colonne.
## Propriétés CSS pour les Tableaux

- `border` : Bordures et ses spéecification(taille, style, couleur etc.)
- `border-collapse` : Fusion des bordures
- `text-align` : Alignement du texte
- `margin et padding` : pour les espacements

N'hésitez pas à expérimenter avec ces concepts pour mieux comprendre leur fonctionnement. Bon codage !

---