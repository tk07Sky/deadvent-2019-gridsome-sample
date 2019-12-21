# deadvent-2019-gridsome-sample

このリポジトリは、[diffeasyアドベントカレンダー2019](https://qiita.com/advent-calendar/2019/diffeasy)で書いた「GridsomeとContentfulを使って、簡単に更新できる静的LPページを作ってみる」という記事のサンプルリポジトリです。

## SET UP

```sh
$ git clone git@github.com:tk07Sky/deadvent-2019-gridsome-sample.git
$ cd deadvent-2019-gridsome-sample
$ npm i
$ touch .env
$ vim .env
```

```
# .env
CONTENTFUL_SPACE_ID=YOUR_SPACE
CONTENTFUL_ACCESS_TOKEN=YOUR_ACCESS_TOKEN
```

## START or BUILD

```sh
# start develop mode
$ npm run develop

# generate static site page
$ npm run build
```