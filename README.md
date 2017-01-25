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