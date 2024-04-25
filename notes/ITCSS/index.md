<!--
vim:spell wrap ts=2 sw=2
-->
# ITCSS

Triangulo Invertido

Métricas y principios


## Principios

  - No usar IDs
  - Patrón componentes UI (dividir el UI en fragmentos)
  - Arquitectura basada en clases

## Métricas

  - De estilos genéricos a específicos
  - De baja especificidad a alta especificidad
  - De Largo alcance a localizado


## Triangulo

  - Magnitud:
    Alcance e impacto en cantidad de elementos
    + -> -
  - Especificidad:
    Fuerza del selector y sus propiedades
    - -> +
  - Claridad:
    Menor abstracción en la semántica e impacto del selector
    - -> +

## Beneficios

  - Estilos globales fáciles de compartir, eficaz y eficientemente
  - Disminución de batallas por estilos
  - Menos redundancia

## Layers

  - Settings
    Variables Globales
    Colores y tamaños
  - Tools
    Funciones globales y mixins
  - Generic
    css común, reset, normalize
  - Elements
    Estilos de selectores
    Nav form Table
  - Objects
    Objetos o contenedores, grids, ccontainer
  - Components
    Component, buttons, carousel, site-nav
  - Trumps
    Estilo de utilidad o ayuda, con !important

