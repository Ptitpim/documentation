WEBPACK
=======

Mode
----

Providing the `mode` configuration option tells webpack to use its built-in optimizations accordingly.

*Possible values for mode are: `none`, `development` or `production` (default).*

Documentation : https://webpack.js.org/concepts/mode/

The `--mode development` flag just adds default Webpack configurations which came with Webpack 4. You wouldn’t need the flag for Webpack 3.

Usage :

Just provide the `mode` option in the config:

```javascript
module.exports = {
  mode: 'production'
};
```

or pass it as a CLI argument:

```bash
webpack --mode=production
```

Ressources
----------

- [The minimal React + Webpack 4 + Babel Setup](https://www.robinwieruch.de/minimal-react-webpack-babel-setup/) (january 18, 2018)
- [rwieruch/minimal-react-webpack-babel-setup](https://github.com/rwieruch/minimal-react-webpack-babel-setup) (github)
- [React Code Style with ESLint + Babel + Webpack](https://www.robinwieruch.de/react-eslint-webpack-babel/) (january 19, 2018)