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

## Atelier : Animation « type card » moderne & responsive (HTML + CSS 2025)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src="css-3.webp" alt="html" width="100px">

---
> **But pédagogique**
>
> * Consolider les bases : `@keyframes`, `transform`, `transition`.
> * Introduire la **syntaxe CSS 2025** (nesting natif, `:scope`, fonctions fluide : `clamp()`, `min()`, `max()`).
> * Pré-parer l’arrivée des **media queries** (Responsivité proprement dite)

---

### 1. Concepts avant de coder

| Terme                         | Rôle                                   | Pourquoi maintenant ?                           |
| ----------------------------- | -------------------------------------- | ----------------------------------------------- |
| `@keyframes`                  | Définit une timeline d’étapes          | Animation principale (apparition, slide).       |
| `transform`                   | Applique un déplacement, scale, rotate | Indispensable pour le « slide ».                |
| `steps / ease / cubic-bezier` | Courbe de vitesse                      | Maîtriser l’allure.                             |
| `transition`                  | Animation courte déclenchée (hover)    | Effet d’amplification sur la carte.             |
| `clamp(min, ideal, max)`      | Taille fluide sans media queries       | Introduction douce à la responsivité.           |
| **Nesting natif** (`&`)       | Écriture imbriquée                     | Syntaxe désormais supportée sans préprocesseur. |

---

### 2. Squelette HTML de base

```html
<main class="grid">
  <article class="card">
    <img src="https://picsum.photos/280" alt="">
    <h2>Robert</h2>
    <p>Développeuse Full-Stack passionnée.</p>
    <button>Me contacter</button>
  </article>
  <!-- dupliquez la <article> pour tester la grille -->
</main>
```

---

### 3. Feuille CSS étape par étape

#### 3.1 Variables & portée (`:root` + `:scope`)

```css
:root {
  --clr-bg: hsl(330 100% 98%);
  --clr-pri: hsl(261 80% 55%);
  --radius : 1.25rem;
}
```

* **Pourquoi ?** Centraliser les couleurs, faciliter la retouche.

#### 3.2 Grille responsive (vous connaissez déjà !)

```css
.grid {
  display: grid;
  gap: 2rem;
  grid-template-columns: repeat(auto-fit, minmax( clamp(260px, 30vw, 400px), 1fr));
  padding: 4rem;
  background: var(--clr-bg);
  place-content: center;
}
```

* **`auto-fit + minmax + clamp`** = grille fluide sans media query.

#### 3.3 Carte : styles statiques + nesting

```css
.card {
  background: white;
  border-radius: var(--radius);
  box-shadow: 0 1rem 2rem hsl(0 0% 0% / .15);
  overflow: hidden;
  width: clamp(260px, 30vw, 400px);
  /* état initial de l'animation */
  opacity: 0;
  transform: translateY(4rem);
  animation: slide-up .9s ease-out forwards;
  /* délai incrémenté via attr style= --i: index*/
  animation-delay: calc(var(--i,0) * .2s);
  will-change: transform;

  & img {
    width: 100%;
    display: block;
  }

  & h2 {
    margin: 1rem 1.5rem 0;
    font-size: clamp(1.2rem, 3vw, 1.6rem);
  }

  & p {
    margin: .5rem 1.5rem 1.5rem;
    line-height: 1.5;
  }

  & button {
    margin: 0 1.5rem 1.5rem;
    padding: .6rem 1.5rem;
    background: var(--clr-pri);
    border: none;
    border-radius: .5rem;
    color: white;
    cursor: pointer;
    transition: transform .3s;
    
    &:hover { transform: translateY(-4px); }
  }

  /* zoom léger de la carte au survol */
  &:hover {
    transform: translateY(-4px) scale(1.02);
  }
}
```

#### 3.4 Animation @keyframes

```css
@keyframes slide-up {
  from { opacity: 0; transform: translateY(4rem) }
  to   { opacity: 1; transform: translateY(0) }
}
```

* **À quoi s’attendre ?** Chaque carte glisse du bas vers le haut en douceur.

---

### 4. Diffuser l’ordre d’apparition

Dans ton HTML, ajoute un incrément simple :

```html
<article class="card" style="--i:0">…</article>
<article class="card" style="--i:1">…</article>
<article class="card" style="--i:2">…</article>
```

* **`calc(var(--i)*.2s)`** décale chaque carte de 0.2 s → effet de cascade.

---
<!-- 
### 5. Pont vers la responsivité / media queries

* Les cartes sont déjà fluides grâce à `clamp` et `grid`.
* **Prochaine leçon** : ajouter un breakpoint pour changer l’animation ou la grille :

```css
@media (width < 600px) {
  .grid { grid-template-columns: 1fr }
  .card:hover { transform: none } /* supprime le zoom mobile */
}
```

* Introduire **container queries** si tu veux aller plus loin (2025).

--- -->

### 6. Ce que vous devez retenir

1. **Animation déclarative** avec `@keyframes`.
2. **Nesting natif** pour écrire un CSS clair.
3. **Unités fluide (`clamp`)** qui préparent la tête aux media queries.
4. Utiliser des **variables CSS** pour la cohérence.

