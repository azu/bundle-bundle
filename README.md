# bundle-bundle

requireしてbundleするだけ

## Installation

    yarn install

## Usage

以下のコマンドでビルドできる

    yarn run build

## プロジェクト構造

- index.js - 読み込む + global(window)に追加する

```js
// window.jQueryとwindow.lodashをはやす
// window.$とindow._をはやす
global.jQuery = global.$ = require("jquery");
global.lodash = global._ = require("lodash");
```

- bundle.js - `yarn run build`でビルドしたもの
    - webpackを使ったシンプルなビルド
- index.html - bundle.jsを読み込んでる
    - window.jQueryなどが使える

## Tips

[webpack](https://webpack.js.org/ "webpack")はconfig.jsなくても引数だけで超簡単なビルドはできる

    Usage: https://webpack.js.org/api/cli/
    Usage without config file: webpack <entry> [<entry>] <output>
    Usage with config file: webpack


## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

MIT