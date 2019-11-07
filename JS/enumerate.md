```js
function doExchange(arr, depth) {
  for (let i = 0; i < arr[depth].length; i++) {
    result[depth] = arr[depth][i];
    if (depth != arr.length - 1) {
      doExchange(arr, depth + 1);
    } else {
      results.push(JSON.parse(JSON.stringify(result)));
    }
  }
}

function enumerate(arr) {
  results = [];
  result = [];
  doExchange(arr, 0);
  return results;
}

const input = [
  ['a', 'b', 'c'],
  ['1', '2', '3'],
  ['x', 'y', 'z'],
];

const output = enumerate(input);

console.log(output);
/*
[
  ['a','1','x'], ['a','1','y'], ['a','1','z'],
  ['a','2','x'], ['a','2','y'], ['a','2','z'],
  ['a','3','x'], ['a','3','y'], ['a','3','z'],
  ['b','1','x'], ['b','1','y'], ['b','1','z'],
  ['b','2','x'], ['b','2','y'], ['b','2','z'],
  ['b','3','x'], ['b','3','y'], ['b','3','z'],
  ['c','1','x'], ['c','1','y'], ['c','1','z'],
  ['c','2','x'], ['c','2','y'], ['c','2','z'],
  ['c','3','x'], ['c','3','y'], ['c','3','z'],
]
*/
```
