## DECLARACIÓN DE VARIABLES

Podemos utilizar variables para almacenar información que luego queremos reutilizar.

Para trabajar con variables en Sass simplemente tenemos que utilizar el símbolo $ para identificar esa variable. Luego podremos hacer referencia a ese nombre en lugar del valor en sí.

 

```scss
// Ejemplo variables SCSS

$base-color: #FFD700;
h1 {
   color: $base-color;
}
```

 

Cuando compilamos Sass, ese trozo de código se convierte en:

 

```css
// Traducido a CSS
h1{
	color: #FFD700;
}
```

  

**¿Qué diferencias hay con las variables de CSS?**

- Si recordamos, podíamos usar variables en CSS del estilo —variable. La diferencia principal es que las variables Sass se compilan mientras las variables de CSS están incluidas en la salida de css.
- Las variables de css pueden tener diferentes valores para diferentes elementos, en caso de las variables Sass solo tienen valor una vez.
- Las variables Sass son *imperativas* , lo que significa que si usa una variable y luego cambia su valor, el uso anterior seguirá siendo el mismo. Las variables CSS SON *declarativas* , lo que significa que si cambia el valor, afectará tanto a los usos anteriores como a los posteriores.
