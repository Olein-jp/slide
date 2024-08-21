---
theme: default
paginate: true
footer: "対面・オンライン同時開催 Toyama WordPress Meetup勉強会第67回 8月21日（水）" 
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
        color: 
    }

    a {
        color: #074073;
        text-decoration: underline;
    }

    section table {
        width: 100% !important;
        display: table;
    }

    footer {
        font-size: .5rem;
        color: gray;
    }
</style>

# WordPress のパターンを理解しよう

---

![bg left](https://olein-design.com/wp-content/uploads/2023/08/kuno_high-quality_square-768x768.jpg)

# 自己紹介

- 久野 晃司（岐阜県岐阜市在住）
- [オレインデザイン](https://olein-design.com)
- フリーランス ウェブ制作者
- [WordPress コントリビューター](https://profiles.wordpress.org/olein/)
- Snow Monkey/unitone
- [hook wp_](https://hook-wp.com/)
- [本、書きました（TT4本）](https://amzn.to/4fKGPWd)

**最近、メルマガはじめました**✉️

---

# アジェンダ

- WordPress のパターンとは
- パターンの種類
- 作り方と活用方法

---

<!--
_backgroundColor: #081226
_color: white
-->

# WordPress のパターンとは

---

# パターンとは

- WordPress 6.4 で導入された
    - 以前は「再利用ブロック」という形で使われていた
- 事前に構成された１つ以上のブロック
- 単なるブロックのグループ
- サイトエディターからテンプレートに挿入したり、ブロックエディターからコンテンツに挿入したりできる

---

# テンプレート・パーツと同じでは？

- テンプレート・パーツは `header.html` といった HTML ファイル
- パターンはテーマ内に用意する際に PHP ファイルのため PHP を記述できる
    - パターン内のテキストを翻訳可能にしたり、画像などの URL を動的に管理することができる

---

<!--
_backgroundColor: #081226
_color: white
-->

# パターンの種類

---

# パターンの種類

- 同期（Synced）
- 非同期（Not Synced）

---

<style scoped>
    h1 {
        color: #0076BA;
    }
</style>

# 同期パターン

- どこで使用しても変更されない
- 旧・再利用ブロックと同じ
- **オリジナルを変更すると配置したすべての同期パターンに反映される**
- WordPress 6.6 から**任意の箇所を上書き可能に設定できる**ようになった

---

<style scoped>
    h1 {
        color: #FEAE00;
    }
</style>

# 非同期パターン

- 配置されたら普通のブロックとして存在する
- ブロックに変更を加えても他のパターンに影響を与えない
- **オリジナルに変更を加えても以前配置したものには影響を及ぼさない**

---

# 同期パターンの上書き機能

- 同期パターンとして登録したパターン内の特定のブロックを任意で上書き可能に設定できる

|6.6 で利用可能ブロック|サポートされる属性|
|:---|:---|
|画像| `url`, `alt`, `title`|
|見出し|`cotnent`|
|段落|`content`|
|ボタン|`url`, `text`, `linkTarget`, `rel`|

---

<!--
_backgroundColor: #081226
_color: white
-->

# 作り方と活用方法

---

# 作り方

- サイトエディター or ブロックエディターから登録
- テーマフォルダの中に `/patterns` ディレクトリを作って PHP ファイルを用意
- プラグインからは `register_block_pattern()` で登録

---

![bg contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/all-about-wordpress-pattern/assets/images/tt4-directory-of-pattern.png)

---

# 利用できるプロパティ例

```
<?php
/**
 * Title: About
 * Slug: twentytwentyfour/page-about-business
 * Categories: page
 * Keywords: starter
 * Block Types: core/post-content
 * Post Types: page, wp_template
 * Viewport width: 1400
 */
?>
```

[Patterns – Block Editor Handbook | Developer.WordPress.org](https://developer.wordpress.org/block-editor/reference-guides/block-api/block-patterns/)

---

# 活用方法

## 非同期パターン

- ページやコンテンツの雛形

## 同期パターン

- CTA や バナーなどの管理

## 同期パターンの上書き機能

- スタイルは共通管理、コンテンツは変わるもの
    - カスタムフィールドを読み込んだブロックを登録する？

---


<!--
_backgroundColor: #081226
_color: white
-->

# 実際に触って確認

---

# 環境の紹介

- WordPress 6.6.1（6.6.0 でもOK）
- WordPress 標準テーマ Twenty Twenty-Four を使用
- プラグインは特に必要なし

---

# やってみること

1. パターンを配置してみる
1. ブロックを配置してパターンに登録してみる（非同期）
1. 同期パターンとして登録してみる
1. 同期パターン内のブロックを上書き可能設定にしてみる

---

# 同じように取り組みたい方

`https://playground.wordpress.net/?blueprint-url=https://raw.githubusercontent.com/Olein-jp/my-wordpress-playground-data/main/blueprints/all-about-wordpress-pattern.json`