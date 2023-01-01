Ahora llega el turno de trabajar con SCSS. Viendo la estructura de la web que queremos desarrollar, vamos a crear los siguientes ficheros con el objetivo de organizar el código:

- main.scss → será el fichero raíz

```scss
@import 'variables';
@import 'mixins'; 
@import 'card';

body{
    background-color: $color-primary;
    padding: $spacing;
    min-height: 100vh;
    font-family: $fonts;
    font-weight: lighter;
    @include flexible;
}
```

- _variables.scss → donde guardaremos todas las variables que usemos

```scss
$color-primary: #E5DED3;
$color-secondary: #0D1623;
$color-thirst: #999;
$color-card-1: white;
$fonts: Arial, sans-serif;
$spacing: 20px;
```

- _mixins.scss → seguro que de algún mixin sacamos provecho

```scss
@mixin flexible {
    display: flex;
    align-items: center;
    justify-content: center;
}
```

- _card.scss → donde guardaremos todos los estilos de la tarjeta

```scss
.card {
    width: 500px;
    background-color: $color-card-1;
    box-shadow: 5px 5px 5px 5px rgba(0,0,0,0.3);
    border-radius: 15px;
    margin: $spacing;
    overflow: hidden;

    &__imagen{
        width: 100%;
    }

    &__body{
        padding: $spacing;
    }

    &__title{
        margin: 0;
        color: $color-secondary;
        text-transform: uppercase;
        font-size: 10px;
    }

    &__subtitle{
        color: $color-secondary;
        font-weight: lighter;
        margin: $spacing 0;
        font-size: 30px;
        font-style: italic;
    }

    &__copy{
        color: $color-thirst;
        font-weight: lighter;
    }

    &__footer{
        padding: $spacing;
        @include flexible;
    }

    &__button{
        color: $color-secondary;
        background-color: $color-card-1;
        border: 1px solid $color-secondary;
        border-radius: 30px;
        padding: 15px;
        font-size: 14px;

        &:hover{
            background-color: $color-secondary;
            color: $color-card-1;   
        }
    }

    &--reverse{
        background-color: $color-secondary;
        .card__title, .card__subtitle{
            color: $color-card-1;
        }

        .card__button{
            color: $color-card-1;
            background-color: $color-secondary;
            border: 1px solid $color-card-1;

            &:hover{
                background-color: $color-card-1;
                color: $color-secondary;
            }
        }
    }
}
```

Por último, crearemos nuestro repositorio con el proyecto e iremos a la configuración para habilitar github pages y así poder compartir nuestro ejercicio.

Para más información sobre como estructurar los elementos de scss os dejamos un artículo donde lo detalla en profundidad:

> https://latteandcode.medium.com/c%C3%B3mo-organizar-los-archivos-sass-de-tu-proyecto-c8b02242d95
