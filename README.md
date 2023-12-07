# @appmana/html-to-jsx

html-to-jsx converts HTML to JSX for use with [React 18.2](facebook.github.io/react/).

# Usage

HTMLtoJSX can be used either as a command-line application or as a Node.js module. To use the command-line version, invoke the `htmltojsx` command:

```
$ htmltojsx --help
Converts HTML to JSX for use with React.
Usage: htmltojsx [-c ComponentName] file.htm

Examples:
  htmltojsx -c AwesomeComponent awesome.htm    Creates React component "AwesomeComponent" based on awesome.htm


Options:
  --className, -c  Create a React component (wraps JSX in React.createClass call)
  --help           Show help
```

To use the Node.js module, `require('htmltojsx')` and create a new instance. This is the same interface as the web-based version:

```js
var HTMLtoJSX = require('htmltojsx');
var converter = new HTMLtoJSX({
  createClass: true,
  outputClassName: 'AwesomeComponent'
});
var output = converter.convert('<div>Hello world!</div>');
```

# Development

Using node 18+:

```shell
corepack enable
yarn install --immutable
yarn run test
```
