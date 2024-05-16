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