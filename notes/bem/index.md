<!--
vim:spell wrap ts=2 sw=2
-->

# BEM

Block, Elements and Modifiers

## Intro

### Block:

Standalone entity that is meaning on its own
Entidad independiente que tiene significado por sí sola.

EX:
 - Header
 - Container
 - Menu
 - Checkbox
 - Input

### Element:

A part of block that has no standalone meaning and is semantically tied to this block

EX:
  - menu item
  - list item
  - checkbox caption
  - header title

### Modifier

A flag on a block or element. Use them to change appearance or behavior#

EX:
  - disabled
  - highlighted
  - checked
  - size big
  - color yellow

## Mix

Logo
Input
Menu
  - menu elements
Button
Input 
  - size big
Button
  - Theme green

### Work

Create a Block element for usual cases and soma more states for different ones.

`block--modifier-value`

EX:

```html
<button class="button">
    Normal button
</button>
<button class="button button--state-success">
    Success button
</button>
<button class="button button--state-danger">
    Danger button
</button>
```

```css
.button {
    display: inline-block;
    border-radius: 3px;
    padding: 7px 12px;
    border: 1px solid #D5D5D5;
    background-image: linear-gradient(#EEE, #DDD);
    font: 700 13px/18px Helvetica, arial;
}
.button--state-success {
    color: #FFF;
    background: #569E3D linear-gradient(#79D858, #569E3D) repeat-x;
    border-color: #4A993E;
}
.button--state-danger {
    color: #900;
}
```

### Benefits

Modularity, Reusability, Structure

## Naming

### Block

Lowercase, digits, letters and dashes, spaces are dashes
Represent a space `.block`
In CSS use just selector, no tag or id


### Element

Lowercase letters, digits, dashes and *underscore*
The name start with the block name plus two underscores plus element name

`.block__elem`

In CSS just use the simple selector without the block nested

**Ok**

```css
.block__elem { color: #343434;}
```

**BAD**
```css
.block .block__elem { color: #343434; }
div.block__elem { color: #343434; }
```


### Modifier

Flags on the blocks or elements, use them to change the appearance, behavior or state

Modifier names may consist lowercase letters, digits, dashes and underscores

CSS class is formed by Block's or element0s name plus two dashes `.block--mod` or
`block__elem--mod` and `block--color-black` with `block--color-red`

Spaces in the mod are replaced by dashes

**Ok**

```html
<div class="block block--mod">...</div>
<div class="block block--size-big block--shadow-yes">...</div>

```

**BAD**
```html
<div class="block--mod">...</div>

```


### Example

```html
<form class="form form--theme-xmas form--simple">
  <input class="form__input" type="text" />
  <input
    class="form__submit form__submit--disabled"
    type="submit" />
</form>
```

```css
.form { }
.form--theme-xmas { }
.form--simple { }
.form__input { }
.form__submit { }
.form__submit--disabled { }
```
