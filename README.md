# Mobx Notes

Mobx bridges reactive and imperative programming

Guiding principle: 'Anything that can be derived from the application state, should be derived. Automatically.'

## Key Concepts

### Observable

Using `@observable` is like turning a value into a spreadsheet cell.

### Computed

Usinge `@computed` decorator, or parameterless functions as property valeus in `extendObservable`, to define values that will automatically be derived when relevant data is modified

### Actions

### Reactions

Similar to a computed value but produces a side effect rather than a new value

Create reactions using observer, autorun, when autorunAsync, reaction

## Resources

* [Readme](https://github.com/mobxjs/mobx/blob/56c3ad276671731505b9100a2f869bfeb1b1e7b6/README.md)
* [Documentation](https://mobxjs.github.io/mobx/index.html)
* [Becoming fully reactive: an in-depth explanation of MobX](https://medium.com/@mweststrate/becoming-fully-reactive-an-in-depth-explanation-of-mobservable-55995262a254#.g6h5oqur4)
