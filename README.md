# webpack_eslint_babel

- WebPack- 4
- React 16
- Redux
-

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

  - "build": "webpack",
  - "dev": "webpack --mode development"

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

## Notes:

- By default npm scripts watch it out inside node_modules/.bin
- webpack requires a `src folder` to pe present in your project
