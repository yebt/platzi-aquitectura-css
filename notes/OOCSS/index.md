<!--
vim:spell wrap ts=2 sw=2
-->
# OOCSS

Object Oriented CSS


## Principles

  - Separar la estructura del diseño
  - Separar contenedor de contenido


### Separar Estructura de Diseño

  - Props de estructura:
    Height, width, margin, padding
  - Props de apariencia
    color, font

```css
/*Struct Props*/
.card {
  width: 10rem;
  height: 15rem;
}

/* Appearance props */
.gray {
  background: gray;
}
```

### Separar contenedor de contenido

Separar las responsabilidades del contenedor y se derroga el estido a su estructura o diseño
