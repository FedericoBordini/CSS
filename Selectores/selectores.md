# Selectores CSS

## ¿Que son los selectores?

Estos son los distintos elementos HTML que seran seleccionados para que se les aplique los valores de las propiedades CSS.

``` css
h1 {
    color: blue;
    background-color: yellow
}

p {
    color: red;
}
```

## Listas de selectores

Si quiero aplicar una misma regla para más de una clase o elemento HTML puedo separarlos por comas (,).

```css
h1, .special {
    color: blue;
}
```

## Tipos de selectores

Existen muchos selectores y depende de las necesidades que tengamos los vamos a utilizar.

### Tipo, clase, id

|Selector| Atributo|
|--------|---------|
|tipo | h1 { }     |
|class|.box { }    |
|id   | #unique { }|

### Selectores de atributos

|Elemento|Atributo|
|--------|--------|
|a       |a[title]|
|a       |a[href="google.com.ar"]|

### Pseudo-classes y pseudo-elements

|Pseudo-classes|Pseudo-elements|
|--------------|---------------|
|a:hover{ }    |p::first-line{}|
|              |               |

### Combinados

En este último grupo podemos combinar distintos elementos que sean hijos directos dentro de nuestro documento.

```css
article > p {
    color: purple
}
```

### Selector universal

Es representado por un asterisco (*) y selecciona todo el documento o lo que embuelbe el elemento padre, vemos en el ejemplo como funciona eliminando todos los margenes que tiene el navegador.

``` css
* {
  margin: 0;
}
```

Para tener un pequeño ejemplo del selector universal fuera de afectar a todo el documento podemos usarlo con, por ejemplo, una pseudo-clase como :first-child. Esto nos permite hacer que todos los primeros hijos sean incluidos y ponerlos en negrita.

``` css
.prueba *:first-child {
    font-weight: bold;
}
```

### Aplicar a un elemento si tiene más de una clase

Podemos aplicar varias clases a un elemento y seleccionarlas individualmente o todas dependiendo si el selector esta presente. Es útil cuando creamos componentes.

``` css
.notebox {
  border: 4px solid #666;
  padding: .5em;
}

.notebox.warning {
  border-color: orange;
  font-weight: bold;
}

.notebox.danger {
  border-color: red;
  font-weight: bold;
}
```

### Selectores ID

Es un poco mas complejo de usar que las clases, dado que solo se puede usar 1 vez por página y en lugar de un punto va el hash (#).

``` css
#one {
  background-color: yellow;
}

h1#heading {
  color: rebeccapurple;
}
```

> [!WARNING]
> Utilizar el mismo ID varias veces en un documento puede parecer que funciona a efectos de estilo, pero no lo haga. Resulta en código inválido, y causará un comportamiento extraño en muchos lugares, además de ser más útil con JavaScript.
