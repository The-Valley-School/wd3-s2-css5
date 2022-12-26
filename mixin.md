### Mixings

Los mixin son fragmentos de código CSS reutilizables a lo largo de nuestro proyecto web. Los creamos una vez y luego solo hay que llamarlos.

Vamos a hacer un ejemplo sencillo en el cual añadimos un color de fondo dentro de una etiqueta

 
```scss
// Creamos el mixin que devuelve el color

@mixin theme(){
	color: red;
}

// lo incluimos dentro de nuestro elemento 

h1 {
	@include theme();
}

```

Un mixin puede tener un argumento

```scss
// Creamos el mixin que devuelve el color elegido

@mixin theme($value-one){
	color: $value-one;
}

// lo incluimos dentro de nuestro elemento

h1 {
	@include theme(red);
}

```
 
o incluir varios: 

 

```scss
// Creamos el mixin que devuelve el color elegido

@mixin theme($value-one, $value-two){
	color: $value-one;
	font-size: $value-two;
}

// lo incluimos dentro de nuestro elemento

header {
	@include theme(red, 22px);
}

```

   

Un uso muy común es para definir tamaños de pantalla con los que trabajar.

 

```scss

$media-mobile: 480px;
$media-tablet: 768px;

@mixin mobile(){
	@media screen and (max-width: $media-mobile) {
    @content;
  }
}

@mixin tablet(){
	@media screen and (max-width: $media-tablet) {
    @content;
  }
}

.header{
	height: 150px;
	@include tablet() {
		height: 100px;
	}
	.nav{
		// otros estilos
	}
}

```

Aprovechamos también para hacer hincapié en el `@content` que nos permite pasar contenido dinámico y usaremos mucho en este tipo de tareas.

```scss
/* CSS */
header {
  height: 150px;
}

@media only screen and (min-width: 768px) {
  .header {
    height: 100px;
  }
}

```

También es de gran ayuda para trabajar con FLEX y GRID

 

```scss
//FLEX

@mixin flexible($dis, $direction, $cut, $just, $align){
    display: $dis;
    flex-flow: $direction $cut;
    justify-content: $just;
    align-items: $align;
}

main{
    @include flexible(flex ,row ,wrap ,center ,center);
}
section{
    @include flexible(flex ,column ,nowrap ,flex-start , flex-end);
}

//GRID

@mixin grid($size, $gap) {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax($size, 1fr));
    gap: $gap;
}

main {
    @include grid(200px, 10px)
}
```

   
