# Webpack blocks - The convenience package

[![JavaScript Style Guide](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)
[![NPM Version](https://img.shields.io/npm/v/webpack-blocks.svg)](https://www.npmjs.com/package/webpack-blocks)

This is the webpack blocks convenience package. It wraps all the most commonly used blocks, so you can install just this single package and have webpack blocks and your favorite blocks set up.


## Usage

Here is a small sample configuration. Instead of requiring from `@webpack-blocks/webpack`, `@webpack-blocks/babel6` and others you just need a single `require()` and a single dependency in your `package.json`.

Of course you can still separately define or install custom blocks and use them as you want.

```js
const {
  addPlugins,
  babel,
  createConfig,
  css,
  defineConstants,
  entryPoint,
  extractText,
  setOutput,
  webpack
} = require('webpack-blocks')

module.exports = createConfig([
  entryPoint('./src/main.js'),
  setOutput('./build/bundle.js'),
  babel(),
  css(),
  defineConstants({
    'process.env.NODE_ENV': process.env.NODE_ENV
  }),
  extractText('css/[name].css'),
  addPlugins([
    new webpack.LoaderOptionsPlugin({ minimize: true })
  ])
])
```

## Included packages

* [assets](https://github.com/andywer/webpack-blocks/tree/master/packages/assets)
* [babel6](https://github.com/andywer/webpack-blocks/tree/master/packages/babel6)
* [dev-server](https://github.com/andywer/webpack-blocks/tree/master/packages/dev-server)
* [extract-text](https://github.com/andywer/webpack-blocks/tree/master/packages/extract-text)
* [postcss](https://github.com/andywer/webpack-blocks/tree/master/packages/postcss)
* [sass](https://github.com/andywer/webpack-blocks/tree/master/packages/sass)
* [typescript](https://github.com/andywer/webpack-blocks/tree/master/packages/typescript)
* [webpack](https://github.com/andywer/webpack-blocks/tree/master/packages/webpack)


## Webpack blocks

Check out the

👉 [Main Documentation](https://github.com/andywer/webpack-blocks)

Released under the terms of the MIT license.