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
