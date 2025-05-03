---
theme: default
paginate: true
footer: "WordPress 6.8 アップデート情報を確認しよう" 
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

# WordPress 6.8 アップデート情報を確認しよう

---

![bg left](https://olein-design.com/wp-content/uploads/2023/08/kuno_high-quality_square-768x768.jpg)

## 自己紹介

- 久野 晃司（岐阜県岐阜市在住）
- フリーランス ウェブ制作者
- [オレインデザイン](https://olein-design.com) 代表
- [WordPress コントリビューター](https://profiles.wordpress.org/olein/)
- Snow Monkey エキスパート／最近は unitone 触ってます
- [hook wp_](https://hook-wp.com/) メンバー
- 岐阜市登録市民団体 Shift 代表

---

## 参考

- [https://www.vektor-inc.co.jp/post/wordpress-6-8-dev-note-note/](https://www.vektor-inc.co.jp/post/wordpress-6-8-dev-note-note/)
- [https://hook-wp.com/podcast/057](https://hook-wp.com/podcast/057)

---

## 管理画面

- 「新規投稿を追加」ラベルが **「投稿を追加」** に変更
- 外観 > パターン が **外観 > デザイン** に変更
- パスワードのハッシュ化アルゴリズムの変更
  - MD5 から bcrypt に変更

---

## エディター

- 表示 に「テンプレートを表示」が追加
- 「スターターパターンの表示」が選択できるようになった
  - インサーター＞パターンで「スターターパターン」パターンカテゴリーが追加された
- 追加CSS 入力エリアが変更になった
- ブロック削除のショートカットが変更になった
- 画像ブロックに「アイキャッチ画像として設定」メニューが追加になった
- クエリーループブロックの先頭固定表示設定された投稿を表示させる選択肢が追加された

---

## 次のメジャーアップデート時期について

- 2026年のどこかで（現在日程は未確定）
- [https://make.wordpress.org/core/6-9/](https://make.wordpress.org/core/6-9/)