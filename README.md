# create-react-icon
Convert one or multiple svg files into React component, inspired by [react-icons](https://github.com/gorangajic/react-icons) project.

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

## License

MIT
