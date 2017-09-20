# babel-plugin-s2s-state-root
[![Build Status](https://travis-ci.org/akameco/babel-plugin-s2s-state-root.svg?branch=master)](https://travis-ci.org/akameco/babel-plugin-s2s-state-root)
[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

> compose state types


## Install

```
$ npm install --save-dev babel-plugin-s2s-state-root
```

### Example

#### IN:

```
```


#### OUT:

```
// @flow
import type { Action as AppAction } from "../app/stateTypes";
import type { Action as BobAction } from "../bob/stateTypes";

export type Action = AppAction | BobAction;
```


### Usage

```
{
  ['s2s-state-root', {
    input: 'containers/**/stateTypes.js',
    output: 'types/state.js',
    globOptions: {}
  }]
}
```

#### input

type: `string` <br>
required: true

glob pattern.

#### output

type: `string` <br>
required: true

outputh path.

#### blobOptions

See https://github.com/isaacs/node-glob#options

## License

MIT © [akameco](http://akameco.github.io)
