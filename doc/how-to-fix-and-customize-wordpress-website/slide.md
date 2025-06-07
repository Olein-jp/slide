---
theme: default
paginate: true
footer: "WordPressサイトを修正・カスタマイズするための最適な方法" 
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

# WordPressサイトを修正・カスタマイズするための最適な方法

---

## 本セッションの目標

- WordPress にはどんな編集方法があるのか知ろう
- **やりたいこと**を**どうやればいいのか**イメージできるようになろう
- 修正・カスタマイズできる意味を知ろう

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

# CMS、そして WordPress とは

---

## CMS とは

- Contents Management System の略
- 翻訳すると「コンテンツ管理システム」
- ウェブサイトのコンテンツを管理するシステムであると言える

---

## WordPress とは

- 世界で最も利用されている CMS であると言える
- オープンソース・ソフトウェア
- 「パブリッシングの民主化」がミッション

---

<!-- _class: section-title -->

# まず自身の WordPress ウェブサイトの状態・環境を把握する

---

## チェックポイント

- あなたのユーザー権限は？
- 利用している WordPress のバージョンは？
- 利用しているテーマは？
- 利用しているエディターは？コンテンツ入力方法は？

これらを把握していますか？🧐

---

### あなたのユーザー権限は？

- 「外観」「プラグイン」「設定」といったメニューが確認できるかどうか
- 管理者権限以外の場合は、その理由を把握しているかどうか

---

### 利用している WordPress のバージョンは？

- ダッシュボード >「概要」で確認
- ツール > サイトヘルス > 情報 > WordPress 内で確認
- 最新バージョンは 6.8.1（スライド作成時）

---

### なぜバージョンを確認するの？

- バージョンによって
  - 多少 UI の違いがある
  - メニューの位置や機能に違いがある場合がある

---

### 利用しているテーマは？

- 外観 > テーマ から有効化しているテーマを確認
- ツール > サイトヘルス > 情報 > 現在のテーマ で確認

---

### なぜテーマを確認するの？

- テーマによって更新方法が全く違う場合がある（稀に？よくある？）
- テーマ特有の機能を使っている場合がある
- オリジナルテーマの場合、全く一般的な方法が通用しない場合がある

---

### 利用しているエディターは？コンテンツ入力方法は？

- 新規投稿もしくは新規固定ページを作る画面を開いて確認する
  - ブロックエディター？クラシックエディター？

- エディターが表示されない？入力してもページに反映されない？
  - カスタムフィールド or テンプレートにハードコーディングの可能性あり

---

<!--　_class: section-title -->

# テーマによる修正方法の違い

---

- クラシックテーマの場合
- ブロックテーマの場合
- オリジナルテーマの場合

---

## クラシックテーマの場合

注：標準エディターを利用しているとする

---

### コンテンツを修正する場合

- 基本は**エディターから修正**する
- できない場合
  - カスタムフィールドが利用されている可能性
  - テンプレートに直接記述されている可能性

---

### レイアウトを修正する場合

- 外観 > カスタマイズ内から変更できる設定を持っているか確認
- テーマ側が変更できる設定を持っていない場合
  - 子テーマなどを使ってコードを書いて解決する（詳細後述）

---

## ブロックテーマの場合

---

### コンテンツを修正する場合

- ブロックエディターで修正する

---

### レイアウトを修正する場合

- 外観 > エディター でサイトエディターを立ち上げて修正する

---

## オリジナルテーマの場合

---

### コンテンツを修正する場合

- ブロックエディターを使えれば標準エディターで
- クラシックエディター（ビジュアル or テキスト）での編集
- カスタムフィールドが用意されている
  - この場合、各種エディターは使えないこともある

---

### レイアウトを修正する場合

- 外観 > カスタマイズ 内で変更できるように作っていることは稀
  - 汎用利用を考えていないとあり得ない
- テンプレートを編集する必要がある場合が多い
  - WordPress テーマ/HTML/CSS/JavaScript などの知識が必要になる場合も

---

<!--　_class: section-title -->

# エディターによる修正方法の違い

---

## ブロックエディターの場合

- フロント側とエディター側で見た目が近しく作られていることも
- 視覚的に編集できる場合が多い
- 便利な反面、最適な形で提供するには技術力も必要に

---

## クラシックエディター

- ビジュアルモードとテキストモードがある
- 2018年12月までの標準エディター
- Classic Editor プラグインを使うことで利用できう

---

## どちらでもない場合

- ページビルダープラグインを利用している場合
  - Elementor、Beaver Builder、Divi など
  - ページビルダーで出来ることしか基本的にできない
- カスタムフィールドを活用している場合
  - 本来はページの**メタ情報**を追加するための仕組み
  - コンテンツを管理するために用意されているわけではない
  - テンプレートなどをカスタマイズしないと修正できない

---

<!--　_class: section-title -->

# カスタマイズしたい時の判断順序

---

## 主なカスタマイズ方法

- （CSSだけなら）追加 CSS 機能から
- 子テーマから
- プラグインから

---

### （CSSだけなら）追加 CSS 機能から

- クラシックテーマなら 外観 > カスタマイズ > 追加 CSS
- ブロックテーマなら 外観 > エディター > スタイルパネル > ３点メニューボタン > 追加 CSS

---

### 子テーマから

- 昔から「WordPress のカスタマイズなら**子テーマ**」みたいに言われてきた
- CSS や JavaScript のファイルを独自に用意し読み込ませられる
- 画像なども利用できる
- **テンプレート上書き機能**が強力
  - メンテナンスを怠ると親テーマのアップデートが適応されず維持されることに…

---

### プラグインから

- **親テーマのメンテナンス性を維持できる仕組み**
- 手軽に有効化・無効化できるので管理が楽
- 子テーマを利用したカスタマイズ方法と若干お作法が違うところがある
- フックを多く持つテーマの場合、特に活用できる方法

---

<!-- _class: section-title -->

# まとめ

---

## 編集可能な範囲を把握することが大切

- 自身の WordPress ウェブサイトが可能な編集範囲を把握する
- 基本的に
  - クラシックテーマであれば**コンテンツ**は編集可能なはず
  - ブロックテーマであれば**レイアウトとコンテンツ**は編集可能
- 標準的なできることを理解して差分を特徴として把握する

---

## 「やりたいこと」と「できること」でバランスを取る

- まずやりたいことを明確にしよう
- それを実現するための方法を知ろう
- それが「できる」のか「できない」のか確認する
  - 「できる」場合はチャレンジする
  - 「できない」場合は「できる」人に依頼をする

---

## ホームページは更新することで存在価値を最大化する

- **コンテンツを更新できる WordPress**は強力
- 小さなことでも随時アップデートすることが大切

---