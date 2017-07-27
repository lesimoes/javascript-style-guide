<img src="https://cdn.rawgit.com/pagarme/brand/9ec30d3d4a6dd8b799bca1c25f60fb123ad66d5b/logo-circle.svg" width="127px" height="127px" align="left"/>

# Pagar.me JavaScript Style Guide

Our style guide is based on [Airbnb's](https://github.com/airbnb/javascript). Differences between them will be described bellow.

<br>

## Semicolons

Do not use semicolons.

## Space before function paren

Wrong:
```js
function transaction(amount) {

}
```

Right:
```js
function transaction (amount) {

}
```

## Comma dangle always on multiline except on functions

Wrong:
```js
const array = [1, 2, 3,]
```

Right:
```js
const array = [1, 2, 3]
```

Wrong:
```js
const array = [
  1,
  2,
  3
]
```

Right:
```js
const array = [
  1,
  2,
  3,
]
```

Wrong:
```js
const obj = {
  a: 1,
  b: 2,
  c: 3
}
```

Right:
```js
const obj = {
  a: 1,
  b: 2,
  c: 3,
}
```

`Dangling comma may cause weird errors when used on functions, you should avoid it.`

Wrong:
```js
Object.assign(
  {},
  b,
  c,
)
```

Right:
```js
Object.assign(
  {},
  b,
  c
)
```

## Maximum Line Length

Avoid having lines of code that are longer than 80 characters (including
whitespace).
