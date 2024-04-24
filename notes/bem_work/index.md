<!--
vim:spell wrap ts=2 sw=2
-->
# Bem Work

  - Bloque:
    Contenedor principal
    Card, button, form, menu, Footer, header
  - Elemento:
    Parte interna del bloque
    icon, text, item, image, input, button (sometimes)
  - Modifier
    Variación de bloque o elemento
    Pseudo clase
    active,big, right, secondary, red

## Naming

- [bloque]
- [bloque]__[elemento]
- [bloque]--[modificador]
- [elemento]--[modificador]
- [block]__[elemento]--[modificador]

## WORK

- Fácil de leer
- Ordenado y modular
- Evitar selectores Anidados

### Case 1

**OK**
block block--mod

**NO**
block--mod


### Case 2

Use levels

**OK**
`card__text, card__icon`

**NO**
`card__text, card__text__icon`


### Case 3

Add children needed styles
Not use selectos of tags, nested or id


## Problems


### Problem 1

Clases del component **A** que ya existe y se va a añadir a un nuevo bloque **B**


```html
<button class="button button--active"></button>
```

```html
<div class="card" >
</div>
```

El componente A se deja con las clases que tiene y se añade a B

### Problem 2

Muchos niveles
Usar el bloque del componente principal y a partir de el, nombrar los elementos

### Problem 3

Los modificadores genéricos no se acoplan al contenedor, como hidden que esconde todo


## BEM + SAS

```css
.card {
  /* ... */
}
.button {
  /* ... */
}
.button--active {
  /* ... */
}
```

```sass
.card {
  &__image {
    /* ... */
  }
}
.image {
  &--active {
    /* .. */
  }
}
```
