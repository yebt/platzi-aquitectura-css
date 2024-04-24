<!--
vim:spell wrap ts=2 sw=2
-->
# DRY

Don't repeat yourself

Reducir la repetición de la información

**BAD**

```css
.card {
  display: flex;
  justify-content: center;
  align-items: center;
  ...
}


.card div {
  display: flex;
  justify-content: center;
  align-items: center;
  ...
}

```

**OK**

```css
.center {
  display: flex;
  justify-content: center;
  align-items: center;
}

card {
  @extend .center
    ...
}

card  div{
  @extend .center
}
```
