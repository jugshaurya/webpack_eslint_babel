# webpack_eslint_babel_prettier

- WebPack- 4
- React 16
- Redux
- Prettier

## How you Should be started ?

- download the repo
- add all the code to your repo
- npm i
- Everything Works! 😍

## How I started ?

- \$ git init
- \$ touch .gitignore
- \$ npm init
  #### webpack
- \$ npm i `webpack webpack-cli` -D
- \$ inside `package.json` add two scripts:

  - "build": "rm -rf dist && webpack",
  - "dev": "rm -rf dist && webpack --mode development"

> > - Now you can build your app using npm run build and get a dist folder
> > - To run it and see the output run node dist/main.js

- \$ `touch webpack.config.js` file to add more comfiguration to our webpack.

  #### babel

- \$ npm i `@babel/cli` `@babel/core` `@babel/preset-env` `babel-loader` -D
- add this to configure webpack with babel inside `webpack.config.js`:

```js
const path = require("path");

module.exports = {
  entry: "./src/index.js",
  output: {
    path: path.join(__dirname, "dist"),
    filename: "main.js",
  },
  module: {
    rules: [
      {
        test: /\.(js|jsx|ts|tsx)$/,
        exclude: /node_modules/,
        use: {
          loader: "babel-loader",
          options: {
            presets: ["@babel/preset-env"],
          },
        },
      },
    ],
  },
};
```

#### eslint - check all code for errors

#### prettier - format our code

## Notes:

- By default npm scripts watch it out inside node_modules/.bin
- webpack requires a `src folder` to pe present in your project

"webpack": "^4.29.3",
"webpack-cli": "^3.2.3",
"@babel/cli": "^7.2.3",
"@babel/core": "^7.2.2",
"@babel/preset-env": "^7.3.1",
"babel-loader": "^8.0.5",
"eslint": "^5.14.0",
"eslint-config-prettier": "^4.0.0",
"prettier": "^1.16.4",

##

"@babel/plugin-proposal-class-properties": "^7.3.3",
"@babel/plugin-proposal-object-rest-spread": "^7.3.2",
"@babel/preset-react": "^7.0.0",
"babel-eslint": "^10.0.1",
"babel-polyfill": "^6.26.0",

"clean-webpack-plugin": "^1.0.1",
"mini-css-extract-plugin": "^0.5.0",
"html-webpack-plugin": "^3.2.0",
"compression-webpack-plugin": "^2.0.0",
"copy-webpack-plugin": "^4.6.0",

"css-loader": "^2.1.0",
"sass-loader": "^7.1.0",
"html-loader": "^0.5.5",
"url-loader": "^1.1.2",
"node-sass": "^4.11.0",

"dotenv-webpack": "^1.7.0",
"webpack-dev-server": "^3.1.14"

"eslint-cli": "^1.1.1",
"eslint-config-airbnb": "^17.1.0",
"eslint-loader": "^2.1.2",
"eslint-plugin-import": "^2.16.0",
"eslint-plugin-jsx-a11y": "^6.2.1",
"eslint-plugin-prettier": "^3.0.1",
"eslint-plugin-react": "^7.12.4",
"lint-staged": "^8.1.4",

"husky": "^1.3.1",
"image-webpack-loader": "^4.6.0",
