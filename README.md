# Webpack Express Example App

The goal of this repo is be an example of a basic but functional app built on Express and Webpack.

If you want to follow along with the course, you will start from the master and switch to the appropriate numbered branches of this repo as needed. The branches are:
- [0-initial-setup](https://github.com/udacity/fend-webpack-content/tree/0-initial-setup)
- [1-install-webpack](https://github.com/udacity/fend-webpack-content/tree/1-install-webpack)
- [2-add-webpack-entry](https://github.com/udacity/fend-webpack-content/tree/2-add-webpack-entry)
- [3-webpack-output-and-loaders](https://github.com/udacity/fend-webpack-content/tree/3-webpack-output-and-loaders)
- [4-webpack-plugins](https://github.com/udacity/fend-webpack-content/tree/4-webpack-plugins)
- [5-webpack-mode](https://github.com/udacity/fend-webpack-content/tree/5-webpack-mode)
- [6-webpack-for-convenience](https://github.com/udacity/fend-webpack-content/tree/6-webpack-for-convenience)

Each one is a step along the path to creating a fully functional webpack setup. In each branch, there will be a documentation file that lists out the steps taken in that branch (each step should also match to a git commit if you look at the history) which you can use as a checklist when setting up your own projects.

## Get Up and Running

Fork this repo, then clone your forked repo down to your computer:

```
git clone -- git@github.com:[your-user-name]/webpack-express.git --
```

`cd` into your new folder and run:
- ```npm install```
- ```npm start``` to start the app
- this app runs on localhost:8080, but you can of course edit that in index.js

Step 0:
npm install
npm start

Step 1:
-Install packages
``` npm i webpack@4.35.3```
``` npm i webpack-cli@3.3.5```
-Following dependencies were added to package.json
``` "webpack": "^4.43.0",```
``` "webpack-cli": "^3.3.11" ```
-To the scripts section of package.json add
```  "build": "webpack" ```
-Add a devDependencies block
```
"devDependencies":{
  "webpack-dev-server": "^3.11.0",
}
```
-Create new file webpack.config.js
-To webpack.config.js add
```
const path = require("path")
const webpack = require("webpack")
module.exports = {
}
```
-Execute
``` npm run build```

Step 2:
-To the webpack.config.js add entry point in the module
```
module.exports = {
	entry: './src/client/index.js',
}
```
-Add client folder to source
-Add index.js file to client
-Add alert to index.js
``` alert('Hi there!');```
- ``` npm run build```
- Dist folder created in project folder
- main.js add to dist folder


Step 3:
-Install babel to the developer version
``` npm i -D @babel/core @babel/preset-env babel-loader```
	-D will install these as development dependencies.

-Create a new babel config file .babelrc
-Config babel
``` { ‘presets’: ['@babel/preset-env'] } ```

-Add rules for using babel in webpack
```
module: {
            rules: [
                    {
                test: '/\.js$/',
                exclude: /node_modules/,
                loader: "babel-loader"
                    }
            ]
    }
```

- Import js files in index.js
- Export from original file

- Add the bundled files to html

- Build again
``` npm run build ```
