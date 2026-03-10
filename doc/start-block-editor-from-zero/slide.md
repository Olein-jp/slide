---
theme: default
paginate: true
footer: "ゼロからはじめるブロックエディター" 
size: 16:9
---

<style>
@import "https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@100..900&display=swap";

section {
    font-family: "Noto Sans JP", sans-serif;
    color: var(--_base);

    /* color palette */
    --_base: #333333;
    --_accesn-01: darkblue;
    --_contrast: #ffffff;
    --_link: #1d35b4;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  color: var(--_accesn-01);
}

h1 {
  font-size: 2rem;
}
h2 {
  font-size: 1.5rem;
}
h3 {
  font-size: 1.25rem;
}

strong {
  font-weight: bold;
  color: var(--_accesn-01);
}

a {
  color: var(--_link);
  text-decoration: underline;
}

section table {
  width: 100% !important;
  display: table;
}

section ul,
section ol {
  padding-left: 1em;
}

section ul > li,
section ol > li {
  margin-bottom: 0.4em;
}

section ul > li > ul,
section ol > li > ol {
  margin-top: 10px;
}

header,
footer {
  font-size: .5rem;
  color: rgba( var(--_accesn-01), .5 );
}

/** スライドタイトル */
section.slide-title {
background-color: var(--_accesn-01);
}
section.slide-title h1 {
  color: var(--_contrast);
  text-align: center;
}

/** セクションタイトル */
section.section-title {
  background-color: var(--_accesn-01);
}
section.section-title h1,
section.section-title h2,
section.section-title p,
section.section-title header,
section.section-title footer,
section.section-title:after {
  color: var(--_contrast);
}

section.slide-title header,
section.slide-title footer,
section.slide-title:after,
section.only-bg-image header,
section.only-bg-image footer,
section.only-bg-image:after {
  display: none;
}

section.big-message {
  background-color: yellow;
  color: var(--_contrast);
}

.column-wrapper {
  display: flex;
  gap: 1em;
}

.column-wrapper > div {
  flex: 1;
}
</style>

<!-- _class: slide-title -->

# ゼロからはじめるブロックエディター

---

## アジェンダ

- ブロックエディターとは
- ブロックエディターの基本的な使い方
- 基本的なブロックを使えるようになるには
- ブロックエディターを活用したカスタマイズの方法

---

![bg left](https://olein-design.com/wp-content/uploads/2023/08/kuno_high-quality_square-768x768.jpg)

# 自己紹介

- 久野 晃司（岐阜県岐阜市在住）
- フリーランス ウェブ制作者
- [オレインデザイン](https://olein-design.com) 代表
- [WordPress コントリビューター](https://profiles.wordpress.org/olein/)
- Snow Monkey エキスパート／unitone
- [hook wp_](https://hook-wp.com/) メンバー
- 岐阜市登録市民団体 Shift 代表

---

<!-- _class: section-title -->

# ブロックエディターとは

---

- 2018年12月 WordPress 5.0 で導入された新しいエディター
- コンテンツを「ブロック」という単位で組み立てていく
  - クラシックエディター：テキストを書いて装飾する
  - ブロックエディター：ブロックを並べる

---

## 強み

- 視覚的に柔軟なコンテンツ作成が可能
  - コードが書けなくてもある程度のページを視覚的に作成可能
- ブロックごとの設定とUI
  - 各ブロックごとに設定を持つ
- 開発者が意図した HTML を確実に保持される
  - テキストモードとビジュアルモードの切り替えによるような破損の心配はない
- ノーコードでのレイアウトが可能

---

## 弱み

- 慣れが必要
- テーマとプラグインの対応
- パフォーマンスの問題
  - ブロックの量が多くなると読み込みや操作が重くなることも


---

<!-- _class: section-title -->

# ブロックエディターの基本的な使い方

---

## ブロックを挿入する方法

- インサーターからブロックを追加
- キーボードショートカットを使う
  - `/` を入力してブロック名を入力

---

## ツールバーを活用する

- ブロックごとに異なるツールバーが表示される
- 基本的な装飾を簡単に行える

---

## 設定・スタイルタブを活用する

- 設定とスタイルタブで可能な設定・装飾を活用しよう
- ブロックによって利用できる機能が異なる

---

## ブロックスタイルを活用する

- ブロックスタイルを使うことで、ブロックの見た目を変更できる
- テーマやプラグインによって提供されるスタイルがある

---

<!-- _class: section-title -->

# 基本的なブロックを使えるようになるには

---

## ブロックでできることを把握する

- 可能な設定と装飾の把握
- たくさん触ってみる（これしかない）
- ある程度触っていくと各ブロックに共通する操作を習得できるようになる

---

## 用途別に考える

- ブロックのカテゴリー別に役割を把握する
  - テキスト、メディア、デザイン、ウィジェット、テーマなど

---

<!-- _class: section-title -->

# ブロックエディターを活用したカスタマイズの方法

---

## 追加CSSの活用

- 利用するテーマスタイルによって方法が異なる
  - クラシックテーマ：カスタマイザーより追加CSS
  - ブロックテーマ：サイトエディターより追加CSS

---

## カスタムブロックの利用

- Lazy Blocks などを使いオリジナルカスタムブロックを用意する
- VK Blocks や Snow Monkey Blocks などのブロックを活用する

---

<!-- _class: section-title -->

## まとめ

---

- クラシックエディターは開発が終了している
- 現在、WordPress の標準エディターは「ブロックエディター」
- WordPress を今後使い続けるならブロックエディターに慣れていくと良い