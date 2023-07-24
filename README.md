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
    <style>
      @media screen and (min-width:480px) {・・・}
      @media screen and (min-width:768px) and (max-width:1024px) {・・・}
      @media screen and (min-width:1024px) {・・・}
    </style>
  </head>
  <body><!-- ページに表示される内容を書く --></body>
</html>
```
というように、本来は色々書かなければならないのですが、DanGoがBootStrapの導入をゆるしてくれたので、
```html
<html>
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width-device-width,initial-scale-1.0" />
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-GLhlTQ8iRABdZLl6O3oVMWSktQOp6b7In1Zl3/Jr59b6EGGoI1aFkw7cmDA6j6gD" crossorigin="anonymous">

    <title>YuwakuAR</title>
  </head>
  <body>
    <!-- ページに表示される内容を書く -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js" integrity="sha384-/mhDoLbDldZc3qpsJHpLogda//BVZbgYuw6kof4u2FrCedxOtgRZDTHgHUhOCVim" crossorigin="anonymous"></script>
  </body>
</html>
```
というように、レスポンシブデザインの記述がこの数行で終わってしまいます。便利ですね。
しかもBootStrapが持っている割といい感じのデザインも使えるようになります。
[BootStrapのドキュメント](https://getbootstrap.jp/docs/5.3/getting-started/introduction/)

## AR,jsについて
今回はLocation-Based ARを活用するので、以下の6~8行目のスクリプトタグを追加する

```html
<html>
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width-device-width,initial-scale-1.0" />
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-GLhlTQ8iRABdZLl6O3oVMWSktQOp6b7In1Zl3/Jr59b6EGGoI1aFkw7cmDA6j6gD" crossorigin="anonymous">
    <script src="https://aframe.io/releases/1.3.0/aframe.min.js"></script>
    <script type='text/javascript' src='https://raw.githack.com/AR-js-org/AR.js/master/three.js/build/ar-threex-location-only.js'></script>
    <script type='text/javascript' src='https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js'></script>
    <title>YuwakuAR</title>
  </head>
  <body>
    <!-- ページに表示される内容を書く -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js" integrity="sha384-/mhDoLbDldZc3qpsJHpLogda//BVZbgYuw6kof4u2FrCedxOtgRZDTHgHUhOCVim" crossorigin="anonymous"></script>
  </body>
</html>
```
これでLocation-Based ARのプログラミングの準備ができました。




