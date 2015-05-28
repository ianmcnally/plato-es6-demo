# plato-es6-demo

A demonstration of using ES6 & Babel with Plato.

Inside `src/` there's a demo `.jsx` and a demo `.js` file written in ES6.

They get compiled to ES5 in the `npm run metrics` task, using Babel.

## Run

1. `npm run metrics` - Compiles source code and builds metrics

## View

1. Open `dist/metrics/report/index.html`

## Notes

1. Normally, Babel will add helper functions to each file when compiling files separately. The [runtime plugin](http://babeljs.io/docs/usage/runtime/) removes the helper functions, and replaces them with requires. This reduces the presumed complexity of each module, and cuts down on file size. (Shoutout to @mnunez903 for the awesome find)

2. There's a sample .jshintrc in this project. I explicitly stated `module`, `exports` and `require` are globals. You can use the `node` globals options, but I opted for only this. Also turned on `globalstrict`.
  - One error jshint reports that is Babel's thing is a `!= null` comparison.