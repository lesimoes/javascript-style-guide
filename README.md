<img src="https://cdn.rawgit.com/pagarme/brand/9ec30d3d4a6dd8b799bca1c25f60fb123ad66d5b/logo-circle.svg" width="127px" height="127px" align="left"/>

# Pagar.me JavaScript Style Guide

Our style guide is based on [Airbnb's](https://github.com/airbnb/javascript). Differences between them will be described bellow.

<br>

## Installing

The rules described in this repository are also available as a eslint
config package. To install the package and its dependencies:

```shell
$ npm install --save-dev eslint@4.7.2 \
                         eslint-plugin-import@2.7.0 \
                         eslint-config-pagarme-base
```

> The peer dependencies specified above have hardcoded versions.
> If you prefer you can use the command
> `npm info eslint-config-airbnb-base@latest peerDependencies`
> to find the exact peer dependencies to install.

To include in the project, create an `.eslintrc` file with at least the
following contents:

```json
{
  "extends": ["pagarme-base"]
}
```

## Rules

### Semicolons

Do not use semicolons.

### Space before function paren

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

### Linebreaks inside function parentheses

Wrong:
```js
transaction(amount,
  installments)
```

Right:
```js
transaction(
  amount,
  installments
)
```

### Comma dangle always on multiline except on functions

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

### Maximum Line Length

Avoid having lines of code that are longer than 80 characters (including
whitespace).
