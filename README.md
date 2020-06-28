# This is a boilerplate template for React with Modern JS Tooling

## Commands to test babel transpiling

```
$(npm bin)/babel ./src/greet.js
$(npm bin)/babel ./src/greet.js --presets=@babel/preset-env

```

### Steps to set up the initial configuration

1. npm init -y (Set up accordingly the values for your package.json)
2. git init
3. npm i -D webpack webpack-cli
4. Create webpack.config.js
5. npm i -D @babel/core @babel/cli @babel/preset-env babel-loader
6. Add the rules for js files to use your babel-loader (webpack.config.js)
7. Include your @babel/preset-env as options in your babel loader configuration (webpack.config.js)
8. npm i -S react react-dom prop-types
9. npm i -D @babel/preset-react
10. Include your react preset as part of the options of your babel-loader configuration (webpack.config.js)
11. npm run build
12. npm i -D html-webpack-plugin
13. Create an index.html under src directory then configure your webpack.config to add the html-webpack-plugin and set the template to that file src/index.html
14. npm i -D webpack-merge
15. Rename your file webpack.config.js to be the base so now called webpack.config.base.js and create two more files webpack.config.dev.js and webpack.config.prod.js and there each one of those will override the configuration for each environment accordingly. Look at the files.
16. Go to your package.json and setup you `build` and `dev` scripts to pass each of the previous configuration files.
17. npm i -D webpack-dev-server
18. Go to your package.json in your `dev` script instead of sending "webpack --watch" now change that for webpack-dev-server and your changes will reflect without have to refresh your browser everytime
19. If you want to hit the app in a different port than 8080 then you can send and object with params in your webpack.config.dev.js file
20. By adding --open after the previous change in your package.json you can see the app open in a new tab in your browser.
21. If you do a breakpoint in your code, you will not see your code as plain as you typed, so to accomplish this and make your life easier debugging you have to add into your webpack.config.dev.js a new key to your object called devtool: 'source-map'
22. npm i -D @babel/plugin-proposal-class-properties
23. Add the previous plugin into the options of your babel-loader, so now can evaluate state from React
24. Let's add a CSS file, you will receive an error, that's because there're no loaders to treat this files, we might need to tell babel how to handle them. So run: npm i -D css-loader style-loader
25. Now let's add a rule in our webpack.config.base.js file to read these files properly.
