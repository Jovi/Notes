### hyphen-case string to camel-case
```js
function camelCased(str) {
    return str.replace(/-([a-z])/g, g => g[1].toUpperCase());
}
```
