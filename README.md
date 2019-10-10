# pretty-stack
![version](https://img.shields.io/badge/version-0.1.0-blue.svg)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/SlimIO/is/commit-activity)
![MIT](https://img.shields.io/github/license/mashape/apistatus.svg)

Pretty Stack Trace to stdout in TTY. Use clean-stack of sindresorhus under the hood to improve the whole experience.

<p align="center">
    <img src="https://i.imgur.com/YSPu6oV.png">
</p>

## Requirements
- [Node.js](https://nodejs.org/en/) v10 or higher

## Getting Started

This package is available in the Node Package Repository and can be easily installed with [npm](https://docs.npmjs.com/getting-started/what-is-npm) or [yarn](https://yarnpkg.com).

```bash
$ npm i @slimio/pretty-stack
# or
$ yarn add @slimio/pretty-stack
```

## Usage example
```js
const prettyStack = require("@slimio/pretty-stack");

const err = new Error("hello world!");
prettyStack(err, true);
// or go with the stack array
prettyStack(err.stack, false);
```

## API

### prettyStack(error: Error | string | string[], printFile?: boolean): void
This method can handle many input types. In case the input is a string it will be splitted by `\n`.

## Dependencies

|Name|Refactoring|Security Risk|Usage|
|---|---|---|---|
|[clean-stack](https://github.com/sindresorhus/clean-stack#readme)|Minor|Low|Cleanup Javascript stack-trace|
|[kleur](https://github.com/lukeed/kleur)|Minor|Low|The fastest Node.js library for formatting terminal text with ANSI colors~!|

## License
MIT
