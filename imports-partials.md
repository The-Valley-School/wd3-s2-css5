### PARTIALS / IMPORTS

Sass nos permite crear pequeños fragmentos de código con partes de SCSS que luego podemos ir reutilizando a lo largo de todo nuestro proyecto web. El enfoque es intentar modularizar al máximo para evitar repetir mucho código y que así, el proyecto sea mas mantenible.

El proceso sería el siguiente.

- Creamos un fichero con el código SCSS que queramos. Es importante que el nombre lleve delante una _

```scss
// _initialize.scss
* {
	margin:0;
	padding: 0;
}
```


- Para incluirlo dentro de otro fichero SCSS hay que utilizar @import y el nombre del archivo sin _ entre ''.

  

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
