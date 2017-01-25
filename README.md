# vue-traning

以下を参考に練習  
http://qiita.com/m0a/items/34df129d6d8991ebbf86

```sh

npm init -y

#ローカルインストール
npm install webpack vue-loader  --save-dev
npm install vue --save

#グローバルインストール
npm install webpack -g

```

make webpack.config.js

```js
// webpack.config.js
module.exports = {
  entry: './src/main.js',
  output: {
    path: "./build",
    filename: 'build.js'
  },
  module: {
    loaders: [
      { test: /\.vue$/, loader: 'vue' },
    ]
  }
}
```

make bellow files
- ./src/main.js
- ./src/app.vue
- index.html

./src/main.js

```js
var Vue = require('vue')
var appOptions = require('./app.vue')
var app = new Vue(appOptions).$mount('#app')
```
./src/app.vue

```js
<template>
  <h1 class="red">{{msg}}</h1>
</template>

<script>
    module.exports = {
        data: function() {
            return {
                msg: 'Hello world!'
            }
        }
    }
</script>

<style>
    .red {
        color: #f00;
    }
</style>
```
index.html

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <title>vue simple sample </title>
</head>

<body>
    <div id="app"></div>
    <script src="build/build.js"></script>
</body>

</html>
```

ファイル修正時に自動でビルドが効くようになる

```sh
webpack --watch
```

vue-router導入

```sh
npm install vue-router --save
```

