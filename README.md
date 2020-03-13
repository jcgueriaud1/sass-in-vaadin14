# Example of SASS file used in Vaadin 14

The SASS files are loaded with webpack.

If you want to reproduce in an other project:
* Install sass-loader and node-sass: ```npm install node-sass scss-loader```
    * This will add these dependencies to package.json
* Update the webpack configuration (webpack.config.js):
```
module: {
        rules: [
            {
                test: /\.scss$/,
                use: [ "raw-loader", "sass-loader"],
            }
        ]
    }, 
```

You can import your SCSS with @CssImport annotation.
If you modify your scss file and reload the page the new style should be applied.
