# Mobx Notes

Mobx bridges reactive and imperative programming

Guiding principle: 'Anything that can be derived from the application state, should be derived. Automatically.'

Want to avoid manual subscription to state changes

A minimal, consistent set of subscriptions can only be achieved if subscriptions are determined at run-time.

Don't cache, derive instead. Derivations from computed values only, these are termed 'reactive' derivations. If a computed value is not reactive, it wil be evaluated on demand, lazily.

Computed values should always be pure functions of the observable app state, that is because the evaluation of these functions always returns the same observable state.

Running computations:
* Trigger recomputation, push derivations onto derivation stack
* May lead to further calculation of computed value depending if already in reactive mode
* 

Propagationg state changes happed by sending stale/ready notifications. The count of stale and ready notificatiosn it kept to ensure that values are reevaluated in order

## Key Concepts

### Observable

Using `@observable` is like turning a value into a spreadsheet cell.

### Computed

Usinge `@computed` decorator, or parameterless functions as property valeus in `extendObservable`, to define values that will automatically be derived when relevant data is modified

Either in reactive or laxy mode

### Actions

Only way to change state

### Reactions

Similar to a computed value but produces a side effect rather than a new value

All reactions happen synchronously

A reaction is basically a computed value that is always in reactive mode.

Create reactions using observer, autorun, when autorunAsync, reaction

## Resources

* [Readme](https://github.com/mobxjs/mobx/blob/56c3ad276671731505b9100a2f869bfeb1b1e7b6/README.md)
* [Documentation](https://mobxjs.github.io/mobx/index.html)
* [Becoming fully reactive: an in-depth explanation of MobX](https://medium.com/@mweststrate/becoming-fully-reactive-an-in-depth-explanation-of-mobservable-55995262a254#.g6h5oqur4)
* [Pure rendering in the light of time and state](https://medium.com/@mweststrate/pure-rendering-in-the-light-of-time-and-state-4b537d8d40b1#.3uvyjzpjs)
* [React, transparent reactive programming and mutable data structures](https://www.youtube.com/watch?v=FEwLwiizlk0)
* [Making React reactive: the pursuit of high performing, easily maintainable React apps](https://www.mendix.com/tech-blog/making-react-reactive-pursuit-high-performing-easily-maintainable-react-apps/)
