# Javascript cheat sheet

For people already confortable with Javascript.

## Performance

Using [`performance.now()`](https://developer.mozilla.org/en-US/docs/Web/API/Performance/now):
```js
const t0 = performance.now();
doSomething();
const t1 = performance.now();
console.log("Call to doSomething took " + (t1 - t0) + " milliseconds.");
```

## Debugging

Spy on property change:
```js
Object.defineProperty(myObj, 'prop', { set: val => debugger })
```

## Functional patterns

Most of these following examples are just ways of using functional assignments instead of assigning directly in forEach loops.
Shape a list of items into an object:
```js
const itemKeyValueList = items.map(item => [item.getName(), myNewObjecValue])
Object.fromEntries(itemKeyValueList))
```

## Misc

Pass value to a callback using a closure:
```js
const myCallback = myValue => <args> => {}
```
