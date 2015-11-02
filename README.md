# split-measure-units

A small function that will separate out the amount from the units in a normal English measurement phrase, and optionally convert it to a different unit

## ES6 Module!
This is authored as an ES6 module and relies on ES6 features. The `main` key in `package.json` points to the transpiled ES5 source, but the `jsnext:main` key points to the ES6 original source. If your environement supports: 

* block scoping (`let` & `const`)
* destructuring (`let [abbott, costello] = ['abbot', 'costello']`)
* ES6 `import` and `export`

Then feel free to use the ES6 source directly.

## Usage
```js
import splitMeasure from 'split-measure-units'

console.log(splitMeasure('1 cup')) // [1, 'cup', 'cup']
console.log(splitMeasure('12 minutes')) // [12, 'minutes', 'minutes']
console.log(splitMeasure('62.45 hampsters')) // [62.45, 'hampsters', 'hampsters']
console.log(splitMeasure('1 gal', 'qt')) // [4, 'qt', 'gal']
```

The method takes two arguments: the measurement and an optional unit to convert to.  For conversions is relies on [convert-units](https://github.com/ben-ng/convert-units/), so see that documentation for what units it can convert. It will also support converting between Farhenheit and Celsius independant of the convert-units library

