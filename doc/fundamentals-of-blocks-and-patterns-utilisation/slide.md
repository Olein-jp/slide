---
theme: default
paginate: true
footer: "ブロックとパターン活用の基礎知識" 
size: 16:9
---

<style>
    @import "https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@100..900&display=swap";

    * {
        font-family: "Noto Sans JP", sans-serif;
        color: #081226;
    }

    h1, h2, h3, h4, h5, h6 {
        color: #081226;
    }

    h1 {
        font-size: 2rem;
    }

    strong {
        text-decoration: underline;
    }

    a {
        color: #074073;
        text-decoration: underline;
    }

    section table {
        width: 100% !important;
        display: table;
    }

    header,
    footer {
        font-size: .5rem;
        color: #808080;
    }

    section.section-title {
        background-color: #081226;
    }
    section.section-title h1,
    section.section-title h2,
    section.section-title p,
    section.section-title header,
    section.section-title footer,
    section.section-title:after {
        color: white;
    }

    section.only-bg-image header,
    section.only-bg-image footer,
    section.only-bg-image:after {
        display: none;
    }

    section.big-message {
        background-color: yellow;
        color: #ffffff;
    }
</style>

# ブロックとパターン活用の基礎知識

---

![bg left](https://olein-design.com/wp-content/uploads/2023/08/kuno_high-quality_square-768x768.jpg)

# 自己紹介

- 久野 晃司（岐阜県岐阜市在住）
- [オレインデザイン](https://olein-design.com) 代表
- 岐阜市登録市民団体 Shift 代表
- フリーランス ウェブ制作者
- [WordPress コントリビューター](https://profiles.wordpress.org/olein/)
- Snow Monkey エキスパート／最近は unitone 触ってます
- [hook wp_](https://hook-wp.com/) メンバー
- [本、書きました（TT4本）](https://amzn.to/4fKGPWd)

---

![bg left height:100%](https://pbs.twimg.com/media/Gdcsdh8bkAAEttT?format=jpg&name=900x900)

# TT5本、執筆中

- 2024年内には出版したい
- 動画解説などは Udemy に出そうか検討中

---

<!-- _class: section-title -->

# ブロックを使うために必要な環境

---

![bg vertical right](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/001.png)

![bg](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/002.png)

# どちらを使っていますか？🙋

- ブロックエディター
- クラシックエディター

---

# ブロックを使うために必要な環境

- ❌ ~~ブロックテーマ~~
- ⭕️ ブロックエディター

<br>ブロックエディターは WordPress 5.0（2018年12月10日リリース）から採用されている標準エディターです。

---

<!-- _class: section-title -->

# コアブロックでレイアウトを組むために<br>必要な"２つ"の知識

---

# 1. コアブロックの役割を理解する

- ❌ 思い通りのレイアウトが組めればどんなブロックを使っても良い
- ⭕️ コアブロックの役割を理解して使い分ける（マークアップ的思考👍）

---

![bg left contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/003.png)

## テキスト

1. 段落 `<p>`
2. 見出し `<h1>`
3. リスト `<ul>`, `<ol>`
4. テーブル `<table>`

---

![bg left contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/004.png)

## メディア

1. 画像 `<figure><img>`
2. カバー `<div>`and more
3. メディアとテキスト<br>`<div><figure><img>`

---

![bg left contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/005.png)

## デザイン

1. グループ `<div>` and more
2. ボタン `<a>`
3. カラム `<div>`

<br>横並び・縦積み・グリッドはグループのバリエーションブロック

---

![bg left contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/006.png)

## ウィジェット

1. 最新の投稿
2. カスタム HTML
3. ショートコード

---

# 2. 基本レイアウトを組む<br>ブロックを理解する

- グループブロック（縦積み・横並び）
- カラムブロック

---

<!-- _class: only-bg-image -->

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/014.jpg)

---

<!-- _class: only-bg-image -->

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/015.jpg)

---

<!-- _class: section-title -->

# コアブロックを使ったレイアウト例

---

<!-- _class: only-bg-image -->

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/010.jpg)

---

<!-- _class: only-bg-image -->

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/011.jpg)

---

<!-- _class: only-bg-image -->

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/012.jpg)

---

<!-- _class: section-title -->

# パターンとは

---

## パターンとは

- 1つ以上のブロックの集合体
- 提供元はさまざま
  - パターンライブラリ（WordPress.org）
  - テーマ
  - プラグイン
  - ユーザー

---

<!-- _class: section-title -->

# パターンへのアクセス

---

<!-- _class: only-bg-image -->

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/007.png)

---

<!-- _class: only-bg-image -->

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/008.png)

---

<!-- _class: only-bg-image -->

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/009.png)

---

<!-- _class: section-title -->

# パターンにはどんな種類があるの？

---

## パターンの種類

- 同期パターン
  - 上書き機能の有無
- 非同期パターン

---

<!-- _class: section-title -->

# どんな時にパターンは活用できるの？

---

## パターンの活用方法

- ページやコンテンツの雛形（非同期パターン）
- CTA やバナーなどの管理（同期パターン）
- スタイリングを一元管理したいコンポーネントの管理（同期パターンの上書き機能）

---

<!-- _class: only-bg-image -->

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/016.jpg)

---

# 同期パターンの上書き機能デモ

---

<!-- _class: section-title -->

# ブロックバインディング

---

## ブロックバインディングとは

- 任意のブロックとカスタムフィールドをはじめとする様々なデータとを結びつけることができる
- Block Bindings API により実現

---

<!-- _class: bg-image -->

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/fundamentals-of-blocks-and-patterns-utilisation/assets/images/013.jpg)

---

時間があれば

## ブロックバインディングのデモ

---

<!-- _class: section-title -->

# まとめ

---

- コアブロックだけで出来ることを理解しておくと良い
  - 出来ることが徐々に増えてきている
- デフォルト機能であるパターンを活用することでカスタムフィールド製造業から離脱できる？
  - ブロックバインディングの活用にも注目

---

## 僕が想像する今後の WordPress

- よりブロックエディター（サイトエディター）が使いやすくなる
- （これまでは書いていたけど）コードを書かずに出来ることが増えていく
- メンテナンス性を考えた制作の重要度が高まる（不良品の波の影響）
  - 安心して「使い続けられる」サイトを作ることが求められる

---

# おわり