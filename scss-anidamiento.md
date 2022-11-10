### ANIDAMIENTO (NESTING)

CSS no es lo más visual y jerárquico del mundo, gracias a SCCS podemos anidar nuestro código, lo que lo hará mas legible y mantenible.

Imaginaos que tenemos el siguiente código en CSS enfocado al típico menú de navegación.

 

```css
nav ul {
	 /* estilos */
}
nav li {
   /* estilos */
}
nav a {
   /* estilos */
}
```

  

Gracias a SCSS podemos hacerlo más legible y cómodo 

  

```scss
nav {
	ul {
		 /* estilos */
	}
	li {
	   /* estilos */
	}
	a {
	   /* estilos */
	}
}
```

  

### CONCATENADO

El símbolo & nos da la posibilidad de concatenar clases, lo que es de gran ayuda para trabajar con metodología BEM 

```scss
// SCSS
a {
  &:hover {
    color: red;
  }
}

.bender {
  margin: 10px;
  &__arms {
		color: red;
	}
}
```

```scss
/* CSS */
a:hover {
  color: red;
}

.bender {
  margin: 10px;
}

.bender__arms {
  color: red;
}
```