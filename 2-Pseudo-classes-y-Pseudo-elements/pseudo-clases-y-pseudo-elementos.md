# Pseudo-classes y Pseudo-elements

## ¿Que es una pseudo-clase?

Ya vimos en el apartado anterior una de estas seleccionando el primer elemento de un tipo específico o si el mouse pasa por encima del mismo, es una clase especial que se aplica a nuestro documento, perfecto para reducir el exceso de clases.

``` css
article p:first-child {
  font-size: 120%;
  font-weight: bold;
}
```

El anterior es un pequeño ejemplo para recordar como se utilizan este tipo de clases especiales. Todas se comportan de la misma forma dirigiendose a una parte específica de tu documento. Revisemos algunos links para conocer diferentes clases:

- [:last-child](https://developer.mozilla.org/en-US/docs/Web/CSS/:last-child)
- [:only-child](https://developer.mozilla.org/en-US/docs/Web/CSS/:only-child)
- [:invalid](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)

### Pseudo-classes para acciones del usuario

En este caso se activan cuando el usuario entra en contacto con alguna parte de nuestra web, desencadenando alguna acción o suceso, podemos ver como ejemplo los dos siguientes aunque existen muchos más

- [:hover](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover)
- [:focus](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus)

```css
a:hover {
  color:hotpink;
}
```

## ¿Que es un pseudo-elemento?

Funcionan de una forma muy similar pero con dos grandes diferencias, la primera es que se escriben con dos signos de dos puntos en lugar de uno (: :) y actuan como si se agregara un nuevo elemento a nuestro HTML. Miremos el ejemplo de uno de ellos ::first-line que dota a todos los hijos de un elemento padre que la primera linea actue de una forma específica independientemente de cuanto ocupa.

```css
article p::first-line {
  font-size: 120%;
  font-weight: bold;
}
```

### Generación de contenidos con ::before y ::after

Hay una propiedad muy especial que convinado con [content](https://developer.mozilla.org/en-US/docs/Web/CSS/content) ponemos agregar contenido antes con `::before` o despues `::after` dependiendo lo que necesitemos.

```css
.box::before {
  content: "This should show before the other content. ";
}
.box::after {
  content: "This should show before the other content. ";
}
```
