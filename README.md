# promise-series

[![NPM version](https://img.shields.io/npm/v/promise-series.svg?style=flat-square)](https://npmjs.com/package/promise-series) [![NPM downloads](https://img.shields.io/npm/dm/promise-series.svg?style=flat-square)](https://npmjs.com/package/promise-series) [![Build Status](https://img.shields.io/circleci/project/egoist/promise-series/master.svg?style=flat-square)](https://circleci.com/gh/egoist/promise-series)

> Run Promise in series.

## Install

```bash
$ npm install --save @rem/promise-series
```

## Usage

```js
const promiseSeries = require('@rem/promise-series')

const sleep = timeout => {
  return new Promise(resolve => {
    setTimeout(() => {
      console.log(new Date())
      resolve()
    }, timeout)
  })
}

// each item returns a Promise
promiseSeries([
  () => sleep(1000),
  () => sleep(2000)
]).then(() => {
  console.log('Completed')
})
```

## API

### promiseSeries(tasks)

#### tasks

Type: `array`

An array of functions which return a Promise.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

[MIT](https://egoist.mit-license.org/) © [EGOIST](https://github.com/egoist)
