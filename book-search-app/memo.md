#本の検索ページを nuxt で作ってみる
https://windii.jp/frontend/nuxt/typescript-book-search-tutorial#i

## まずはテンプレートを作ってみる

vue init nuxt-community/typescript-template book-search-app
そのフォルダの中に入り、npm i する
そのあとで例によって npm run dev

## プリプロセッサを使ってみる

試しに Pug と Sass を使う
そのために以下でインストール
npm install --save-dev pug@2.0.3 pug-plain-loader node-sass sass-loader
pug-plain-loader は pug を html に変換するもの
node-sass は sass をコンパイルするもの
sass-loader は css に変換する

## bootstrap+Vue を使う

npm i bootstrap-vue --save
で導入する

## config の修正

nuxt.config.js を設定する

### 以下を中の modules に追記した

"~/modules/typescript.js",
"bootstrap-vue/nuxt",

## 画面を作る

### まずはレイアウト

まずは default の template を触る
toggleable はなんかサイズ指定できるっぽい
BV でヘッダーをレイアウトに挿入

### 次にコンポーネント

@Component({})って？
typescript のコンポーネント宣言
nuxt-property-decorator って何だよ？
Nuxt.js と Vue を TypeScript と連携させるライブラリ
@Prop() book って？
変数引き継ぎかなって印象

モジュール足らないって怒られた
npm install -g npm-install-missing を追加あとで
関係なかった
npm-install-missing

, '~/modules/typescript.js'
ってとこ消したら動いたけど何で何だろうね？

##

https://note.mu/r82/n/n8d07926f6aaf

サーバーサイドレンダリングについては勉強だな
勉強した結果についてこちらに記載する
https://medium.com/@sundaycrafts/%E3%83%A6%E3%83%BC%E3%82%B6%E3%83%BC%E4%BD%93%E9%A8%93%E3%82%92%E5%90%91%E4%B8%8A%E3%81%95%E3%81%9B%E3%82%8B%E3%82%B5%E3%83%BC%E3%83%90%E3%83%BC%E3%82%B5%E3%82%A4%E3%83%89%E3%83%AC%E3%83%B3%E3%83%80%E3%83%AA%E3%83%B3%E3%82%B0javascript-%E6%AD%B4%E5%8F%B2%E3%81%A8%E5%88%A9%E7%82%B9-df68cd7cd991
ブラウザ側で動かなかった js をサーバー側で動かして、html を吐き出すこと
ユニバーサル JavaScript
アイソモーフィック JavaScript
も同じ意味なんだってさ

パフォーマンスとか、seo とかのメリットがある
でも日本語の情報が少なかったりエラーハンドリングが必要だったり、サーバーの設定を node ように設定したりと厄介
