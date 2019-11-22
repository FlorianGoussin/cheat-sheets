# Redux basics
`Tutorial link`[https://www.robinwieruch.de/javascript-reducer]
`Tutorial examples link`[https://github.com/rwieruch/javascript-reducer]

## Reducer

In essence a reducer function is expressed as `(state, action) => newState`
State Transition: 
* The state is immutable so it doesn't change directly. The reducer is a pure function that returns a new state.
* A reducer can have conditional state transitions.

## Action

An action comes with a mandatory type property and an optional payload:
* the type property chooses the contitional state transition
* the payload provides information for the state transition
