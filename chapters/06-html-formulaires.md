# 06 Html Formulaires


## Cours 5 : Les Formulaires en HTML


### Les Formulaires en HTML

Les formulaires en HTML permettent aux utilisateurs d'interagir avec une page web en fournissant des informations qui peuvent être envoyées à un serveur pour traitement. Structure du Formulaire

```html Le formulaire est encadré par la balise <form> qui définit le début et la fin du formulaire. Les éléments du
```

formulaire sont contenus à l'intérieur de cette balise. Éléments du Formulaire

```html 1. Champs de Texte (<input type="text">) : Ces champs permettent aux utilisateurs de saisir du texte. Ils sont définis avec l'attribut type égal à "text". Par exemple : <label for="nom">Nom :</label> <input type="text" id="nom" name="nom"> 2. Champs de Nombre (<input type="number">) : Ces champs permettent aux utilisateurs de saisir des nombres. L'attribut type est défini à "number". Exemple : <label for="age">Age :</label> <input type="number" id="age" name="age"> 3. Champs d'E-mail (<input type="email">) : Ces champs sont destinés à la saisie d'adresses e-mail. L'attribut type est défini à "email". Exemple : <label for="mail">Mail :</label> <input type="email" id="mail" name="mail"> 4. Champs de Téléphone (<input type="tel">) : Ces champs sont utilisés pour les numéros de téléphone. L'attribut type est défini à "tel". Exemple : <label for="telephone">Numéro de TEL :</label> <input type="tel" id="telephone" name="telephone" placeholder="+221 77 889 89 90">
```

Autres Types de Champs et Attributs Voici une liste d'autres types de champs et d'attributs couramment utilisés dans les formulaires HTML :

**Types de Champs :**

```code password : Pour les mots de passe. url : Pour les URL. file : Pour téléverser des fichiers. radio : Pour les options mutuellement exclusives. checkbox : Pour les options multiples. date : Pour les dates. time : Pour les heures. color : Pour les sélecteurs de couleur.
```


**Attributs Importants :**

```code required : Indique que le champ doit être rempli avant de soumettre le formulaire. disabled : Désactive un élément de formulaire. placeholder : Affiche un texte de rappel dans un champ de saisie. readonly : Rend un champ de texte en lecture seule. multiple : Permet de sélectionner plusieurs options dans un menu déroulant ou avec des cases
```

à cocher.

```code min et max : Définit les valeurs minimale et maximale pour les champs numériques.
```


### Champs de Sélection


```code Menu Déroulant (<select>) : Les menus déroulants permettent aux utilisateurs de choisir parmi plusieurs options. Ils sont définis avec la balise <select> et contiennent des balises <option> pour chaque choix.
```

Exemple :

```sql <label for="pays">Pays :</label> <select id="pays" name="pays"> <option value="senegal">Sénégal</option> <option value="france">France</option> <option value="usa">USA</option> </select> Zone de Texte (<textarea>) : Les zones de texte permettent aux utilisateurs de saisir du texte sur plusieurs
```

lignes. Exemple :

```code <label for="message">Message :</label> <textarea id="message" name="message" rows="4" cols="50"></textarea>
```


### Attributs Additionnels

Voici quelques attributs supplémentaires qui peuvent être utilisés pour personnaliser les champs de formulaire

```code Attributs pour <select> : size : Définit le nombre de lignes visibles dans le menu déroulant. multiple : Permet de sélectionner plusieurs options en même temps. Attributs pour <textarea> : rows : Définit le nombre de lignes de texte visibles dans la zone de texte. cols : Définit le nombre de colonnes de texte visibles dans la zone de texte.
```


### Types de Champs de Formulaire Supplémentaire :


```html Champ de Recherche (<input type="search">) : Utilisé pour les champs de recherche avec des
```

fonctionnalités spéciales comme la saisie semi-automatique.

```html Champ de Range (<input type="range">) : Permet aux utilisateurs de sélectionner une valeur
```

numérique à partir d'une plage spécifiée.

### Attributs Additionnels :


```code Attribut pattern : Permet de définir une expression régulière pour valider le contenu d'un champ de
```

texte.

```code Attribut autocomplete : Indique au navigateur s'il doit activer la fonction d'auto-complétion pour un
```

champ de formulaire.

```code Attribut autofocus : Place automatiquement le curseur de texte dans un champ de formulaire
```

lorsqu'une page est chargée.

```html Attribut form : Permet de spécifier à quel formulaire appartient un élément de formulaire, même s'il n'est pas directement contenu dans la balise <form>.
```

En combinant ces éléments et attributs, les formulaires HTML permettent de collecter des informations de manière structurée et conviviale pour l'utilisateur.

## Exercices pratiques

> Mets en pratique ce que tu viens d'apprendre avant de passer au chapitre suivant.

### Exercice 1 — Application directe

Applique les notions vues dans ce chapitre sur un exemple concret de ton choix.

**Consigne :** Réalise l'exercice correspondant à ce chapitre et valide ta compréhension avant de continuer.

### Exercice 2 — Questions de compréhension

- Quel est le concept principal de ce chapitre ?
- Donne un exemple d'utilisation concrète en contexte professionnel.
- Quelle notion t'a semblé la plus difficile ? Comment l'as-tu abordée ?

### Checklist avant de continuer

- J'ai lu et compris le contenu du chapitre
- J'ai réalisé au moins un exercice pratique
- Je peux expliquer le sujet à quelqu'un d'autre
