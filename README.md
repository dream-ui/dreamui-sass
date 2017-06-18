# tools_sass: common mixin、selector's lib

### Features

> Zero Pollution

This lib use sass mixin and placeholder-selector to ensure your project code is pure. And We don't generate any unuseful css code.

> Perfect Compatibility

This lib is compatible with lower version of the browsers, such as flex、transform、animation and other css attributes.

### Develop Mode

```
$ yarn install
$ yarn test:watch
$ yarn test:liveload
```

### Install

* NPM

```bash
npm add tools_sass
# or
yarn add tools_sass
```

* GIT-Submodule (Recommend)

```
$ mkdir public_modules
$ git submodule add https://github.com/borenXue/tools_sass.git public_modules/tools_sass

/** ~ Optional ~
 * Add npm-script for auto install this lib.
 * Modify script field of package.json file to add preinstall-script.
 */
 "script": {
    "preinstall": "git submodule init; git submodule update;",
 }
```

* GIT-Subtree

```bash
## TODO:
```

### Usage

```
@import 'public_modules/tools_sass/index.scss'

/**
 *  scss syntax examples
 */
.fill-parent {            // placeholder-selector example
  @extend %fill-parent;
}

.fill-parent {            // mixin example
  @include display-flex;
}

/**
 *  sass syntax examples
 */
.fill-parent            // placeholder-selector example
  @extend %fill-parent

.fill-parent            // mixin example
  +display-flex
```

### mixin list

### placeholder-selector list

## Changelog

Details changes for each release are documented in the [release notes](https://github.com/borenXue/tools_sass/releases).

### LICENCE

[MIT](https://opensource.org/licenses/MIT)

Copyright (c) 2017-present, Boren.Xue <xueboren001@outlook.com>
