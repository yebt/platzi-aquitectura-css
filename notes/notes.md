<!--
vim:spell wrap ts=2 sw=2
-->
# Architecture CSS



## BEM


## SOLID

### Single Responsibility Principle

Una clase solo debe cambiar por una razón.

```css
/* Responsibility of the form */
.button {
    border-radius: 2rem;
}

.button--secondary {
    background-color: gray;
    color: black;
}
```

### Open - Closed Principle

Las entidades de software deben estar:
 - abiertas para extensión
 - cerradas para modificación

**BAD**

```css
.button {
    border-radius: 2rem;
}
.button--secondary {
    @extend .button--sm;
    background-color: gray;
    color: black;
}
```

Se está heredando una mala modificación
impidiendo la extensión de este y generando modificaciones


### Liskov Substitution

Un objeto puede ser reemplazado por un subobjeto sin romper el programa

```css
.button {
    border-radius: 2rem;
}

.button--secondary {
    @extend .button;
    background-color: gray;
    color: black;
}
```
