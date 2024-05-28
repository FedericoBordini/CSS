# Combinadores

Lo último que se vera de selectores son los combinadores, que nos permite unir cada uno de los selectores entre sí.

## Combinador descendente

Combina dos selectores de forma que el segundo es el que se ve afectado al tener un elemento antepasado (padre, abuelo, bisabuelo, etc) coincidiendo con el primer selecto.

```css
.box p {
  color: red;
}
```

## Combinador hijo

Solo coincide con los elementos que combienen con el segundo selector que sean hijos directos del primer elemento, los que esten por debajo no seran contados.

```css
article > p
```

## Combinador de hermano siguiente

A diferencia del anterior este coincide con el segundo selector que sea hermano del primero.

``` css
p + img
```

Si escribimos cualquier otra cosa entre medio del `p + img` va perder el efecto que queramos darle, asi tambien si escribimos en otro lado ese códgio vamos a heredar su efecto.

## Combinador de hermano posterior

Si queremos seleccionar hermanos que no sean directamente adyacentes tenemos esta opción para seleccionar todos los que vengan independientemente del lugar o que elemento este en el medio.

```css
p ~ img
```

## Nesting selectores

Nos permite crear selectores más complejos que tenemos un apartado entero en el link [CSSnesting](https://developer.mozilla.org/en-US/docs/Web/CSS/Nesting_selector).

```css
p {
  & img {
  }
}
/* This is parsed by the browser as */
p img {
}
```
