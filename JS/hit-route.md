```js
/**
 * route:
 * /A/B/C
 * /A/:id1/b/:id2
 * /A/*
 */

function hitRoute(route, path) {
    return new RegExp('^' + route.replace(/:[A-Za-z0-9]+/g, '[A-Za-z0-9-_]+').replace(/\*/g, '\\S+').replace(/\//g, '\\\/') + '$').test(path);
}
```
