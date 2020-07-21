This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

Steps followed during the process:

### `npm install`
### `npm i -D tailwindcss postcss-cli autoprefixer`
### `npx tailwind init tailwind.js --full ` (config file for css)
###  `create config file "postcss.config.css" and add following code`
`const tailwindcss = require('tailwindcss')

module.exports = {
    plugins: [
        tailwindcss('./tailwind.js'),
        require('autoprefixer')
    ]
}`
### `create assets folder in src and two files, tailwind.css and main.css`
### `add follwoing code to tailwind.css`
`@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";`

### `replace following code to package.json under scripts`
`"scripts": {
    "start": "npm run watch:css && react-scripts start",
    "build": "npm run build:css && react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "build:css": "postcss src/assets/tailwind.css -o src/assets/main.css",
    "watch:css": "postcss src/assets/tailwind.css -o src/assets/main.css"
  }`

### `npm start`

# Here is a screenshot of the prototype UI

