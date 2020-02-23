setup site directory

npm init
npm install --save @babel/core
npm install --save @babel/node
npm install --save @babel/preset-env

mk file .babelrc
   ->
    {
    "presets": ["@babel/preset-env"]
}

usually $node src/myfile
ES6 isn't natively supported in node so instead use
to build -- not 
$ npx babel-node src/myfile.js

or for repel:
npx babel-node

//Dev dependencies for node
install ESLint
npm install --save-dev eslint
npx eslint --init
npm install --save-dev eslint-plugin-immutable

.eslintrc >> add entry for immutable, and update rules 
module.exports = {
  env: {
    browser: true,
    es6: true,
  },
  extends: [
    'airbnb-base',
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parserOptions: {
    ecmaVersion: 2018,
    sourceType: 'module',
  },
    plugins: ['immutable',
  ],
  rules: {
    'immutable/no-mutation': 2
  },
};
},
    plugins: ['immutable',
  ],


to run eslint, use
npx eslint .

or run regular js with babel
npx @babel/node <filename>
