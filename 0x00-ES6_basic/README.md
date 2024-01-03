## ES6 Basics


ES6 stands for ECMAScript 6. ECMAScript was created to standardize JavaScript, and ES6 is the 6th version of ECMAScript, it was published in 2015, and is also known as ECMAScript 2015.

JavaScript ES6 brings new syntax and new awesome features to make your code more modern and more readable. It allows you to write less code and do more. ES6 introduces us to many great features like arrow functions, template strings, class destruction, Modules… and more.

## Learning Objectives
0. What ES6 is
0. New features introduced in ES6
0. The difference between a constant and a variable
0. Block-scoped variables
0. Arrow functions and function parameters default to them
0. Rest and spread function parameters
0. String templating in ES6
0. Object creation and their properties in ES6
0. Iterators and for-of loops


## Project requirements
0. All your files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x
0. Allowed editors: vi, vim, emacs, Visual Studio Code
0. All your files should end with a new line
0. A README.md file, at the root of the folder of the project, is mandatory
0. Your code should use the js extension
0. Your code will be tested using the Jest Testing Framework
0. Your code will be analyzed using the linter ESLint along with specific rules that we’ll provide
0. All of your functions must be exported


## Work environment setup
0. machine: Ubuntu 18.04 LTS
0. Node version: v12.22.12
0. npm version: v6.14.16


you can install node from your apt repo with the below command

$ sudo apt-get install -y nodejs

# or install from the github

$ curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
$ sudo bash nodesource_setup.sh
$ sudo apt install nodejs -y

# to check version installed

$ node -v
$ npm -v

## Insatalling jest, Babel and ESLint
0. ESLint insatallation guide
$ npm install --save-dev jest
$ npm install --save-dev babel-jest @babel/core @babel/preset-env
$ npm install --save-dev eslint

##Configurations
0. create a file pakage.json and add copy-paste this code
{
  "scripts": {
    "lint": "./node_modules/.bin/eslint",
    "check-lint": "lint [0-9]*.js",
    "dev": "npx babel-node",
    "test": "jest",
    "full-test": "./node_modules/.bin/eslint [0-9]*.js && jest"
  },
  "devDependencies": {
    "@babel/core": "^7.6.0",
    "@babel/node": "^7.8.0",
    "@babel/preset-env": "^7.6.0",
    "eslint": "^6.4.0",
    "eslint-config-airbnb-base": "^14.0.0",
    "eslint-plugin-import": "^2.18.2",
    "eslint-plugin-jest": "^22.17.0",
    "jest": "^24.9.0"
  }
}
0. create a file babel.config.js and copy-paste this code
module.exports = {
  presets: [
    [
      '@babel/preset-env',
      {
        targets: {
          node: 'current',
        },
      },
    ],
  ],
};
0. create a file called .eslintrc.js and cop-paste this code
module.exports = {
  env: {
    browser: false,
    es6: true,
    jest: true,
  },
  extends: [
    'airbnb-base',
    'plugin:jest/all',
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parserOptions: {
    ecmaVersion: 2018,
    sourceType: 'module',
  },
  plugins: ['jest'],
  rules: {
    'no-console': 'off',
    'no-shadow': 'off',
    'no-restricted-syntax': [
      'error',
      'LabeledStatement',
      'WithStatement',
    ],
  },
  overrides:[
    {
      files: ['*.js'],
      excludedFiles: 'babel.config.js',
    }
  ]
};
0. now run the command
$ npm install
**AFTER THIS IS DONE A node_module would be in your current directory containing all packages installed

## Author

## BIN ABDOOL
