# create-react-icon
[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![Downloads][downloads-image]][downloads-url]
[![js-standard-style][standard-image]][standard-url]

Convert one or multiple svg files into inline-svg React component, inspired by [react-icons](https://github.com/gorangajic/react-icons) project.

If you are wondering what the benefit is to use inline svg in React component, please check this post [Creating an SVG Icon System with React](https://css-tricks.com/creating-svg-icon-system-react/).

## Installation

```sh
$ npm install create-react-icon -g
```

## Usage

```sh
$ create-react-icon ./alert.svg dist
$ create-react-icon ./*.svg dist
```

## Result

Your source svg file:

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M200.4 54.1c-1.9-18.7 8.4-32.9 25.8-32.9h63.1c17.4 0 27.7 14.2 25.8 32.9l-27.7 242.2c-1.9 17.4-13.5 28.3-29.6 28.3s-27.7-11-29.6-28.3L200.4 54.1zm57.3 313.1c32.2 0 56 23.8 56 54.8v1.3c0 30.9-23.8 54.8-56 54.8s-56-23.8-56-54.8V422c0-31 23.8-54.8 56-54.8z"/></svg>

```

Becomes to :

```js
import React from 'react'
import Icon from 'react-icon-base'

export default (props) => {
  return (
    <Icon viewBox='0 0 512 512' {...props}>
      <title id='alert'>{props.title || 'alert'}</title>
      <g><path d="M200.4 54.1c-1.9-18.7 8.4-32.9 25.8-32.9h63.1c17.4 0 27.7 14.2 25.8 32.9l-27.7 242.2c-1.9 17.4-13.5 28.3-29.6 28.3s-27.7-11-29.6-28.3L200.4 54.1zm57.3 313.1c32.2 0 56 23.8 56 54.8v1.3c0 30.9-23.8 54.8-56 54.8s-56-23.8-56-54.8V422c0-31 23.8-54.8 56-54.8z"/></g>
    </Icon>
  )
}
```

## How to use icons

```js
import AlertIcon from 'alertIcon'

export default (props) => {
   return (<div>
     <AlertIcon title='alert icon' /> Manage my Collections
  </div>)
}
```

## Roadmap

* Make the base component configurable

## License

MIT

[npm-image]: https://img.shields.io/npm/v/create-react-icon.svg?style=flat-square
[npm-url]: https://npmjs.org/package/create-react-icon
[travis-image]: https://img.shields.io/travis/envato/create-react-icon/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/envato/create-react-icon
[downloads-image]: http://img.shields.io/npm/dm/create-react-icon.svg?style=flat-square
[downloads-url]: https://npmjs.org/package/create-react-icon
[standard-image]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[standard-url]: https://github.com/feross/standard
