[![CircleCI](https://circleci.com/gh/codeforjapan/mapprint/tree/master.svg?style=svg)](https://circleci.com/gh/codeforjapan/mapprint/tree/master)


給水所/お風呂/洗濯（ランドリー）マップ 印刷向け
===

こちらの [給水所/お風呂/洗濯（ランドリー）マップ ](https://www.google.com/maps/d/u/0/viewer?mid=17BQwZDvJhDQ9OKZfakI-2PsyIaGdDtRx&ll=34.395888541511006%2C132.9701334&z=11
) を、印刷向けに最適化したサイトのソースコードです。

https://codeforjapan.github.io/mapprint/

から実際のページを確認できます。

## おばあちゃんの手に届くまで
このプロジェクトで作られたデータは、さまざまな人々の手を経て、困っているおばあちゃんのところに届きます。

![kamimap_180713.png](source/images/kamimap_180713.png)


## Help Wanted!!

Issues にあるいろいろな修正にご協力いただけると嬉しいです。
詳しくは[こちら](./CONTRIBUTE.md)



## 開発環境の構築方法

### Requirement

- ruby >= 2.2.6
- bundler
- node.js >= 6.0.0
  - OSXでbundlerがうまく入らな無い方は[この辺](https://qiita.com/tokimari/items/feda1ed61f2d8b5b317c)を、node.jsが入らない方は[この辺](https://qiita.com/yn01/items/d1fa10dbe4850f7cd693)などをご参照ください


### 環境構築

```
$ git clone git@github.com:codeforjapan/mapprint.git
$ cd mapprint
$ npm install
$ bundle install --path=vendor/bundle
$ bundle exec middleman build
```

### テスト

```
$ npm run lint
$ npm test
```

### 起動

```
$ bundle exec middleman server
```
http://localhost:4567 で見れるはず

参考

### デプロイ
```
$ bundle exec middleman deploy
```

(このリポジトリへの push 権限が必要。
github pages で作られているので、gh-pages ブランチが更新されます。)







## CI/CD

Runnable only macOS and Linux Distros

[Using the CircleCI Local CLI \- CircleCI](https://circleci.com/docs/2.0/local-cli/)

### 設定ファイルのテスト

```
$ circleci config --verbose validate -c .circleci/config.yml
```

### ローカルビルド

Dockerがインストールされて利用出来る状態であればローカルで実行してみることも出来ます。

**現在動作しません**

```
# $ circleci build
```



## 参考

- [Middleman: 作業を効率化するフロントエンド開発ツール](https://middlemanapp.com/jp/)
  - [Middleman: The Development Cycle](https://middlemanapp.com/basics/development-cycle/)
  - [Middleman: Build & Deploy](https://middlemanapp.com/basics/build-and-deploy/)
- [Middleman: Hand\-crafted frontend development](https://middlemanapp.com/)
  - [Middleman: 開発サイクル](https://middlemanapp.com/jp/basics/development-cycle/)
  - [Middleman: ビルド & デプロイ](https://middlemanapp.com/jp/basics/build-and-deploy/)



