# Creating React App

While the project calls for allowing the use of [Create React App](https://github.com/facebook/create-react-app), I have decided to start from scratch, giving me practice setting things up from scratch.

##### Setup

- [x] create package.json `npm init`
- [x] create .gitignore
- [x] public/index.hmtl starter

##### [Babel](https://babeljs.io/docs/en/next/babel-preset-react)

We need to make sure the code we write can be compiled.

- [x] ```bash
  npm install --save-dev @babel/core
  ```
  
- [x] ```bash
  npm install --save-dev @babel/cli
  ```
  
- [x] ```bash
  npm install --save-dev @babel/preset-env
  ```

- [x] ```bash
  npm install --save-dev @babel/preset-react
  ```

- [x] In the project root, create a file called `.babelrc`.

  ```json
  {
    "presets": ["@babel/env", "@babel/preset-react"]
  }
  ```

  

##### [Webpack](https://webpack.js.org/guides/installation/)



- [x] ```bash
  npm install --save-dev webpack
  ```

- [x] ```bash
  npm install --save-dev webpack-cli
  ```

- [x] ```bash
  npm install --save-dev style-loader css-loader
  ```

- [x] ```bash
  npm install --save-dev webpack-dev-server
  ```

- [x] ```bash
  npm install --save-dev babel-loader
  ```

- [ ] Create `webpack.config.js` at the root of the project

```js
const path = require("path");
const webpack = require("webpack");

module.exports = {
  entry: "./src/index.js",
  mode: "development",
  module: {
    rules: [
      {
        test: /\.(js|jsx)$/,
        exclude: /(node_modules|bower_components)/,
        loader: "babel-loader",
        options: { presets: ["@babel/env"] }
      },
      {
        test: /\.css$/,
        use: ["style-loader", "css-loader"]
      }
    ]
  },
  resolve: { extensions: ["*", ".js", ".jsx"] },
  output: {
    path: path.resolve(__dirname, "dist/"),
    publicPath: "/dist/",
    filename: "bundle.js"
  },
  devServer: {
    contentBase: path.join(__dirname, "public/"),
    port: 3000,
    publicPath: "http://localhost:3000/dist/",
    hotOnly: true
  },
  plugins: [new webpack.HotModuleReplacementPlugin()]
};
```

##### React

- [ ] ```bash
  npm install react react-dom
  ```

- [ ] ```bash
  npm install react-hot-loader
  ```

- [x] create `index.js` in the `src` directory

  ```js
  import React from "react";
  import ReactDOM from "react-dom";
  import App from "./App.js";
  ReactDOM.render(<App />, document.getElementById("root"));
  ```

- [x] create another file in `src` called `App.js`

  ```js
  import React, { Component} from "react";
  
  class App extends Component{
    render(){
      return(
        <div>
          <h1>Would You Rather</h1>
        </div>
      );
    }
  }
  
  export default App;
  ```

  

##### Run App

- [x] Add in build to **package.json**

  ```json
    "scripts": {
      "dev": "webpack-dev-server --mode development",
      "build": "webpack --mode production"
    },
  ```

  To run the app:

  - for dev: `npm run dev`
  - for production: `npm run production`