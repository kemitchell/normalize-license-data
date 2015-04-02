# normalize-license-data 

clean up licenses from package.json files and the npm registry

## Installation

Download node at [nodejs.org](http://nodejs.org) and install it, if you haven't already.

```sh
npm install normalize-license-data --save
```

## Usage

```js
var normalize = require("normalize-license-data")

normalize(null)
// => null

normalize('')
// => null

normalize('MIT')
// => {name: 'MIT', url: 'http://opensource.org/licenses/MIT'}

normalize('BSD')
// => {name: 'BSD', url: 'http://opensource.org/licenses/BSD-2-Clause'}

normalize('unfamiliar')
// => {name: 'unfamiliar'}

normalize({name: 'wtfpl', url: 'https:///wtfpl.net'})
// => {name: 'wtfpl', url: 'https:///wtfpl.net'}

normalize({type: 'wtfpl', url: 'https:///wtfpl.net'})
// => {name: 'wtfpl', url: 'https:///wtfpl.net'}

normalize('https://custom-license.com')
// => {name: 'custom-license.com', url: 'https:///custom-license.com'}

```

## Tests

```sh
npm install
npm test
```

## Dependencies

- [is_js](https://github.com/arasatasaygin/is.js): micro check library
- [lodash.clone](https://github.com/lodash/lodash): The modern build of lodash’s `_.clone` as a module.
- [oss-license-name-to-url](https://github.com/npm/oss-license-name-to-url): Convert shorthand OSS license names to opensource.org URLs
- [schemeless](https://github.com/zeke/schemeless): Remove the parts of URLs that humans don&#39;t really need to see

## Dev Dependencies

- [code](https://github.com/hapijs/code): assertion library
- [mocha](https://github.com/mochajs/mocha): simple, flexible, fun test framework
- [package-json-to-readme](https://github.com/zeke/package-json-to-readme): Generate a README.md from package.json contents
- [standard](https://github.com/feross/standard): JavaScript Standard Style


## License

MIT

_Generated by [package-json-to-readme](https://github.com/zeke/package-json-to-readme)_
