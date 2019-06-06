## nuxtでブログを作ってみる
https://qiita.com/hitsuji-haneta/items/7e41bf5cdfde55b826a4
を参考に
yarn global add @vue/cli-init
で、vue-cliをインストールする必要があった

## プロジェクト立ち上げ
vue init nuxt-community/starter-template nuxt_blog
って入力する

nuxrtとはvue.jsアプリケーションを構築するためのフレームワーク

### yarnってなに？
進化したnpmって理解でいる

## テンプレートをつくっていく
とりあえずテンプレートエンジンなどは使わない
改善するファイルは2つ
1つはleyouts/default.vue
もう１つはpagesのindex.vue
それから記事の埋め込みにpages/blog/_slug.vue


### 役所は？
pagesに何かテンプレートを入れると自動的にroutesに反映されるらしい？
本当かよ？
buildしたら確かにできてた




## 最後にpugとstylusで書き換える
### 参考
https://qiita.com/amishiro/items/38fe1b102d7e91a93ada

### ちなみにstylusとは？
sassとsassのいいとこ取りのものらしい
