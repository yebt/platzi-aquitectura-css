<!--
vim:spell wrap ts=2 sw=2
-->
# SOLID

Using SOLID POO concept in CSS

## Single responsibility Principle

Las clases de CSS solo deben tener una razón para cambiar
La clase de **bloques** de BEM deben contener solo lo necesario de su bloque
sin cargar responsabilidades de modificaciones

Los elementos solo se encargan de si mismos y su acople

Finalmente el modificador solo puede controlar la modificación y el estado de atributos ante
el state del elemento
  
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
  
## Open - Close Principle

Abierto a extensión y cerrado para modificación

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

Es dado por la extensión de más modificadores para el bloque sin cargar
extensión modificada a un modificador existente
En el caso anterior el modificador de tamaño está afectando al de color

## Liskov Substitution Principle

Un objeto puede ser reemplazado por un subobjeto sin romper el programa

En algunos casos, la clase de bloque puede ser extendida en su modificador
dado que su uso cargará las propiedades principales del bloque y cargar el modificador

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

```html
<div class="button--secondary"> </button>
```

Button secondary está extendiendo el comportamiento del button genérico

## Interface Segregation Principle

No se debe obligar a ningún código a depender de métodos que no utiliza

```css
.button {
    border-radius: 2rem;
}

.button--secondary {
    @extend .button;
    background-color: gray;
    color: black;
    border-radius: 1.4rem; /* Deja inutilizado el .button */ 
}
```

##  Dependency Inversion Principle


Los módulos de alto nivel no deben deben depender de módulos de bajo nivel.
Ambos deben depender de abstracciones.

**Bad**

```css
.card div .title {
    border-radius: 2rem;
}

```

**OK**

```css
.card__title {
    border-radius: 2rem;
}

```

El sistema de bloques, elementos y modificadores permite la identificación de elementos
adyacentes al bloque, porque lo que no es necesario especificar de ids o etiquetas.
