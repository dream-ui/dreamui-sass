# tools_sass: common mixin、selector's lib

> [Demos](http://xueboren.com/dreamui/sass-demos/)


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
git remote add tools_sass https://github.com/borenXue/tools_sass.git
$ git subtree add --prefix=public_modules/tools_sass tools_sass master
$ git subtree pull --prefix=public_modules/tools_sass tools_sass master
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


### Selector List


| Selector | Desc |
| -------- | ---- |
| fill-parent | ---- |
| fill-width | ---- |
| fill-height | ---- |
| max-fill-parent | ---- |
| single-line-ellipsis | ---- |
| flex-center | ---- |
| flex-center-inline | ---- |
| flex-left | ---- |
| flex-space-between | ---- |
| flex-h | ---- |
| flex-v | ---- |
| text-force-break | ---- |
| model-fixed-full | ---- |
| vcenter | ---- |
| model-absolute-full | ---- |
| uppercase | ---- |



### Mixin List


| Module | SubModule | Mixin Name | Demo |
| ---------- | ---------- |
| Border-Box |
|  | -- | square | square(200px) |
|  | -- | circle | circle(200px) |
|  | -- | box-shadow | box-shadow(0 0 3px #525252) |
|  | border-radius | border-radius | border-radius(8px) |
|  |  | border-top-right-radius | border-top-right-radius(8px) |
|  |  | border-top-left-radius | border-top-left-radius(8px) |
|  |  | border-bottom-right-radius | border-bottom-right-radius(8px) |
|  |  | border-bottom-left-radius | border-bottom-left-radius(8px) |
|  |  | border-top-radius | border-top-radius(8px) |
|  |  | border-bottom-radius | border-bottom-radius(8px) |
|  |  | border-left-radius | border-left-radius(8px) |
|  |  | border-right-radius | border-right-radius(8px) |
|  | thin-border | thin-border | thin-border(red, 'all', initial, after) |
|  |  | thin-border-all | thin-border-all(red) |
|  |  | thin-border-top | thin-border-top(red) |
|  |  | thin-border-bottom | thin-border-bottom(red) |
|  |  | thin-border-left | thin-border-left(red) |
|  |  | thin-border-right | thin-border-right(red) |
| Text |
|  | -- | text-force-break | text-force-break() |
|  | -- | single-line-ellipsis | single-line-ellipsis() |
|  | -- | multi-line-ellipsis | multi-line-ellipsis(3) |
|  | -- | placeholder | placeholder { ... } |
| Flex |
|  | -- | display-flex | display-flex() |
|  | -- | display-inline-flex | display-inline-flex() |
|  | -- | display-flex-important | display-flex-important() |
|  | -- | flex-direction | flex-direction(3) |
|  | -- | flex-wrap | flex-wrap(nowrap) |
|  | -- | flex | flex(1) |
|  | -- | flex-flow | flex-flow(nowrap) |
|  | -- | align-items | align-items(stretch) |
|  | -- | align-self | align-self(auto) |
|  | -- | align-content | align-content(stretch) |
|  | -- | justify-content | justify-content(stretch) |
|  | -- | flex-order | flex-order(3) |
|  | -- | responsive-grid-break | responsive-grid-break(.a-cls, 800px) |
| Transition |
|  | core | transition | transition(height 300ms ease-in) |
|  | -- | transition-delay | transition-delay(300ms) |
|  | -- | transition-duration | transition-duration(300ms) |
|  | -- | transition-timing-function | transition-timing-function(ease-in) |
|  | -- | transition-property | transition-property(height) |
|  | -- | transition-transform | transition-transform(height, width) |
| Transform |
|  | core | transform | transform(scaleY(.5)) |
|  | core | transform-origin | transform-origin(0, 0) |
|  | -- | scale | scale(1, .5) |
|  | -- | scaleY | scaleY(.5) |
|  | -- | scaleX | scaleX(1) |
|  | -- | rotate | rotate(45deg) |
|  | -- | translate | translate(6px, 2px) |
|  | -- | translateX | translateX(6px) |
|  | -- | translateY | translateY(2px) |
|  | -- | translate3d | translate3d(6px, 2px, 5px) |
|  | -- | translateX | translateX(5px) |
|  | -- | skew | skew(1px, 2px) |
| Animation |
|  | -- | animation | animation(3s linear 1s slidein) |
|  | -- | animation-duration | animation-duration(3s) |
|  | -- | animation-direction | animation-direction(alternate-reverse) |
|  | -- | animation-timing-function | animation-timing-function(ease-in) |
|  | -- | animation-fill-mode | animation-fill-mode(both) |
|  | -- | animation-name | animation-name(test-name) |
|  | -- | animation-iteration-count | animation-iteration-count(3) |
| UI |
|  | -- | xui-row | xui-row(): .xui-row、.xui-col-0 ~ .xui-col-100 |
|  | -- | xui-progressing | xui-progressing(): .xui-progressing-0 ~ .xui-progressing-100 |
| Others |
|  | -- | appearance | appearance(none) |
|  | -- | user-select | user-select(none) |
|  | -- | linear-gradient | linear-gradient(to left top, blue, red) |

## Changelog

Details changes for each release are documented in the [release notes](https://github.com/borenXue/tools_sass/releases).

### LICENCE

[MIT](https://opensource.org/licenses/MIT)

Copyright (c) 2017-present, Boren.Xue <xueboren001@outlook.com>
