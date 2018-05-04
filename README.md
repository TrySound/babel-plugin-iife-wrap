# babel-plugin-iife-wrap [![Build Status](https://travis-ci.org/TrySound/babel-plugin-iife-wrap.svg?branch=master)](https://travis-ci.org/TrySound/babel-plugin-iife-wrap)

> Wrap file with iife and add `'use strict;'` (by inheriting from `babel-plugin-transform-strict-mode`).


**Warning**: this plugin is incompatible with [babel-plugin-transform-es2015-typeof-symbol](https://www.npmjs.com/package/babel-plugin-transform-es2015-typeof-symbol) which is in most babel presets, see [this issue](https://github.com/TrySound/babel-plugin-iife-wrap/issues/2) for details. Pull requests are welcome.


## Install

With [npm](https://npmjs.org/package/babel-plugin-iife-wrap) do:

```
npm i babel-plugin-iife-wrap --D
```


## Example

### Input

```js
window.a = 1;
```

### Output

```js
;(function () {
  window.a = 1;
}());
```


## Usage

In your Babel configuration:

```json
{
  "plugins": ["iife-wrap"]
}
```

_Note that Webpack outputs a bundle wrapped with iife by default._


## Contributing

Pull requests are welcome. If you add functionality, then please add unit tests
to cover it.


## License

MIT © [Bogdan Chadkin](https://github.com/trysound)
