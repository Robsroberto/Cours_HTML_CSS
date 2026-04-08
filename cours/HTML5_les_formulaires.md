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

# Cours 5 : Les Formulaires en HTML
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ


---

### Les Formulaires en HTML

Les formulaires en HTML permettent aux utilisateurs d'interagir avec une page web en fournissant des informations qui peuvent être envoyées à un serveur pour traitement.

#### Structure du Formulaire

Le formulaire est encadré par la balise `<form>` qui définit le début et la fin du formulaire. Les éléments du formulaire sont contenus à l'intérieur de cette balise.

#### Éléments du Formulaire

1. **Champs de Texte (`<input type="text">`)** : Ces champs permettent aux utilisateurs de saisir du texte. Ils sont définis avec l'attribut `type` égal à `"text"`. Par exemple :
   ```html
   <label for="nom">Nom :</label>
   <input type="text" id="nom" name="nom">
   ```

2. **Champs de Nombre (`<input type="number">`)** : Ces champs permettent aux utilisateurs de saisir des nombres. L'attribut `type` est défini à `"number"`. Exemple :
   ```html
   <label for="age">Age :</label>
   <input type="number" id="age" name="age">
   ```

3. **Champs d'E-mail (`<input type="email">`)** : Ces champs sont destinés à la saisie d'adresses e-mail. L'attribut `type` est défini à `"email"`. Exemple :
   ```html
   <label for="mail">Mail :</label>
   <input type="email" id="mail" name="mail">
   ```

4. **Champs de Téléphone (`<input type="tel">`)** : Ces champs sont utilisés pour les numéros de téléphone. L'attribut `type` est défini à `"tel"`. Exemple :
   ```html
   <label for="telephone">Numéro de TEL :</label>
   <input type="tel" id="telephone" name="telephone" placeholder="+221 77 889 89 90">
   ```

#### Autres Types de Champs et Attributs

Voici une liste d'autres types de champs et d'attributs couramment utilisés dans les formulaires HTML :

- **Types de Champs :**
  - `password` : Pour les mots de passe.
  - `url` : Pour les URL.
  - `file` : Pour téléverser des fichiers.
  - `radio` : Pour les options mutuellement exclusives.
  - `checkbox` : Pour les options multiples.
  - `date` : Pour les dates.
  - `time` : Pour les heures.
  - `color` : Pour les sélecteurs de couleur.

- **Attributs Importants :**
  - `required` : Indique que le champ doit être rempli avant de soumettre le formulaire.
  - `disabled` : Désactive un élément de formulaire.
  - `placeholder` : Affiche un texte de rappel dans un champ de saisie.
  - `readonly` : Rend un champ de texte en lecture seule.
  - `multiple` : Permet de sélectionner plusieurs options dans un menu déroulant ou avec des cases à cocher.
  - `min` et `max` : Définit les valeurs minimale et maximale pour les champs numériques.



### Menu Déroulant (`<select>`) : 

Les menus déroulants permettent aux utilisateurs de choisir parmi plusieurs options. Ils sont définis avec la balise `<select>` et contiennent des balises `<option>` pour chaque choix. Exemple :
   ```html
   <label for="pays">Pays :</label>
   <select id="pays" name="pays">
       <option value="senegal">Sénégal</option>
       <option value="france">France</option>
       <option value="usa">USA</option>
   </select>
   ```

### Zone de Texte (`<textarea>`) :

Les zones de texte permettent aux utilisateurs de saisir du texte sur plusieurs lignes. Exemple :
   ```html
   <label for="message">Message :</label>
   <textarea id="message" name="message" rows="4" cols="50"></textarea>
   ```


- **Attributs pour `<select>` :**
  - `size` : Définit le nombre de lignes visibles dans le menu déroulant.
  - `multiple` : Permet de sélectionner plusieurs options en même temps.

- **Attributs pour `<textarea>` :**
  - `rows` : Définit le nombre de lignes de texte visibles dans la zone de texte.
  - `cols` : Définit le nombre de colonnes de texte visibles dans la zone de texte.



### Types de Champs de Formulaire Supplémentaire :
- **Champ de Recherche (`<input type="search">`) :** Utilisé pour les champs de recherche avec des fonctionnalités spéciales comme la saisie semi-automatique.
- **Champ de Range (`<input type="range">`) :** Permet aux utilisateurs de sélectionner une valeur numérique à partir d'une plage spécifiée.

### Attributs Additionnels :
- **Attribut `pattern` :** Permet de définir une expression régulière pour valider le contenu d'un champ de texte.
- **Attribut `autocomplete` :** Indique au navigateur s'il doit activer la fonction d'auto-complétion pour un champ de formulaire.
- **Attribut `autofocus` :** Place automatiquement le curseur de texte dans un champ de formulaire lorsqu'une page est chargée.
- **Attribut `form` :** Permet de spécifier à quel formulaire appartient un élément de formulaire, même s'il n'est pas directement contenu dans la balise `<form>`.


En combinant ces éléments et attributs, les formulaires HTML permettent de collecter des informations de manière structurée et conviviale pour l'utilisateur.