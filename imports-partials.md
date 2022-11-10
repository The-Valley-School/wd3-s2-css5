### PARTIALS / IMPORTS

Sass te permite crear pequeños fragmentos de código con partes de SCSS que luego podamos ir reutilizando a lo largo de todo nuestro proyecto web. El enfoque es intentar modularizar al máximo para evitar repetir mucho código y que el proyecto sea mas mantenible.

El proceso sería el siguiente.

- Creamos un fichero  con el código SCSS que nosotros deseemos, es importante que el nombre lleve delante un _

  

```scss
// _initialize.scss
* {
	margin:0;
	padding: 0;
}
```

 

- Para incluirlo dentro de otro fichero SCSS bastará con utilizar @import y el nombre.

  

```scss
@import 'initialize';

h1 {
	color: red;
}
```

 

- Esto, tras la compilación dará como resultado:

  

```scss
* {
	margin:0;
	padding: 0;
}

h1 {
	color: red;
}
```
