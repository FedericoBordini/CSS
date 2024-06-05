# Cascada, Especificidad y Herencia

## Normas contradictorias

Para comprender CSS al completo tenemos que entender sus siglas primero Cascading Style Sheets (hoja de estilo en cascada) siendo la primer palabra que vamos a ver dado que es la mas importante. Cuando estemos trabajando en nuestros proyectos y ver como el CSS no actua como esperamos es porque estamos creando dos reglas que aplican valores distintos a la misma propiedad. Esto convinado con la especifidad determina que se mostrara cuando existan estos conflictos.

## Cascada

Stylesheets [cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade) - básicamente el orden de las reglas importa demasaido para CSS, tanto que cuando dos reglas se aplican al mismo selector con igual especificidad se utilizara la última que definida.

```html
    <h1>This is my heading.</h1>
    <style>
        h1 {
    color: red;
    }
        h1 {
    color: blue;
    }
    </style>
```

En este ejemplo se ve que tienen el mismo selector pero se aplicara la relga `blue` a nuestro `<h1>` dado que es lo último que declaramos.

## Especificidad

Stylesheets [Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)Es un algoritmo que utiliza el navegador para decidir que valor se aplicara a un elemento, en el caso de que varios bloques de estilos apunten a la misma propiedad, mientras más específico sea mas preponderancia tendrá esa regla.

```html
<h2 class="main-heading">This is my heading.</h2>
    <style>
        .main-heading {
            color: red;
        }
        
        h2 {
            color: blue;
        }
    </style>
```

## Herencia

Es básicamente que algunos elementos son padres y los hijos heredan algunas propiedades.

```html
<p>As the body has been set to have a color of blue this is inherited through the descendants.</p>
<p>We can change the color by targeting the element with a selector, such as this <span>span</span>.</p>
<style>
    body {
    color: blue;
    }

    span {
    color: black;
    }
</style>
```

En el ejemplo vemos como todas las letras van a heredar ese color azul, pero especificamente dijimos que el  `<span>` va tener color negro.
