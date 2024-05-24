# @patrten/velit-cum <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS Set? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isSet = require('@patrten/velit-cum');
assert(!isSet(function () {}));
assert(!isSet(null));
assert(!isSet(function* () { yield 42; return Infinity; });
assert(!isSet(Symbol('foo')));
assert(!isSet(1n));
assert(!isSet(Object(1n)));

assert(!isSet(new Map()));
assert(!isSet(new WeakSet()));
assert(!isSet(new WeakMap()));

assert(isSet(new Set()));

class MySet extends Set {}
assert(isSet(new MySet()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@patrten/velit-cum
[npm-version-svg]: https://versionbadg.es/inspect-js/@patrten/velit-cum.svg
[deps-svg]: https://david-dm.org/inspect-js/@patrten/velit-cum.svg
[deps-url]: https://david-dm.org/inspect-js/@patrten/velit-cum
[dev-deps-svg]: https://david-dm.org/inspect-js/@patrten/velit-cum/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@patrten/velit-cum#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@patrten/velit-cum.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@patrten/velit-cum.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@patrten/velit-cum.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@patrten/velit-cum
[codecov-image]: https://codecov.io/gh/inspect-js/@patrten/velit-cum/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@patrten/velit-cum/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@patrten/velit-cum
[actions-url]: https://github.com/patrten/velit-cum/actions
