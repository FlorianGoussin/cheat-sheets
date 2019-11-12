# Javascript cheat sheet

For people already confortable with Javascript.

## Debugging

Spy on property change:
```js
Object.defineProperty(myObj, 'prop', { set: val => debugger })
```
