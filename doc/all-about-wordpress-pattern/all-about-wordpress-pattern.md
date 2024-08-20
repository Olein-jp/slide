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

# 本日のアジェンダ

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
- WordPress 6.6 から任意の箇所を上書き可能に設定できるようになった

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

<!--
_backgroundColor: #081226
_color: white
-->

# 作り方と活用方法

---

# 作り方

- サイトエディター or ブロックエディターから登録
- テーマフォルダの中に `/patterns` ディレクトリを作って PHP ファイルを用意
- プラグインからは `[register_block_pattern()](https://developer.wordpress.org/block-editor/reference-guides/block-api/block-patterns/)` で登録

---

# 利用例



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
1. 同期パターン内のブロックを上書き可能設定してみる

---

# 同じように取り組みたい方

`https://~`