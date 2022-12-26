El uso de @extend nos permite compartir un conjunto de propiedades CSS de un selector a otro.

```scss
%message-shared {
	border: 1px solid #ccc;
	padding: 10px;
	color: #333;
}

.message {
	@extend %message-shared;
}

.success {
	@extend %message-shared;
	border-color: green;
}
```

## OPERADORES

SCSS también nos permite hacer operaciones sobre las propiedades.

```scss
.container {
	display: flex;
}

.article {
	width: 600px / 960px * 100%;
}
```
