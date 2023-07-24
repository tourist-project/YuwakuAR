# YuwakuAR
湯涌温泉でAR体験ができるWebアプリを制作するためのリポジトリ

## HTMLの書き方
HTMLは様々な要素全体が`<html>`タグで囲まれたWebページを構成する電子文書です。
主に見出し(`<h1>`,`<h2>`,`<h3>`)タグや段落(`<p>`)タグなどから構成されるページの本体部分`<body>`と
ページの内容自体には表示されないものの、ページが持っていなければならない情報を記述する`<head>`に分けられて記述することになります。

## ARアプリとして記述しなければならないもの
1. レスポンシブデザインのための`<meta>`タグの`viewport`
```html
<html>
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width-device-width,initial-scale-1.0" />
    <title>YuwakuAR</title>
  </head>
  <body><!-- ページに表示される内容を書く --></body>
```
