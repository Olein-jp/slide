---
theme: default
paginate: true
header: "安心してサイトを運営するためのWordPressセキュリティの基礎知識"
footer: "Gifu WordPress Meetup #74" 
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

    header,
    footer {
        font-size: .5rem;
        color: #808080;
    }

    section.section-title {
        background-color: #081226;
    }
    section.section-title h1,
    section.section-title header,
    section.section-title footer,
    section.section-title:after {
        color: white;
    }
</style>

# 安心してサイトを運営するためのWordPressセキュリティの基礎知識

---

![bg left](https://olein-design.com/wp-content/uploads/2023/08/kuno_high-quality_square-768x768.jpg)

# 自己紹介

- 久野 晃司（岐阜県岐阜市在住）
- [オレインデザイン](https://olein-design.com)
- フリーランス ウェブ制作者
- [WordPress コントリビューター](https://profiles.wordpress.org/olein/)
- Snow Monkey/unitone
- [hook wp_](https://hook-wp.com/) メンバー
- [本、書きました（TT4本）](https://amzn.to/4fKGPWd)

**最近、メルマガはじめました**✉️

---

# アジェンダ

- WordPress セキュリティとは
- セキュリティ設定の基本
- アップデートの重要性
- 信頼できるプラグインの活用
- バックアップという保険
- ユーザー管理と権限設定
- セキュリティに対する意識向上
- 今日から始められるセキュリティ対策

---

<!--
_class: section-title
-->

# WordPress セキュリティとは

---

## WordPress とは

- コンテンツマネージメントシステム（CMS）の１つ
- グローバルシェアは約43%
- [日本国内シェアは82%以上](https://w3techs.com/technologies/segmentation/cl-ja-/content_management)
- 本セッションは WordPress.org（インストール型）を想定した内容

---

## WordPress のよくある利用例

- 個人ブログやビジネス用ウェブサイトなど
- 専門家ではない個人（社内web担当者含む）または管理委託業者など
- 独自ドメイン利用、レンタルサーバーで稼働
- レンタルサーバーが提供する自動インストール機能を利用

---

![bg left](https://images.unsplash.com/photo-1460408037948-b89a5e837b41)

## WordPress は自分の家と考えよう

- 自分が責任を持って**管理**する
- 自分が責任を持って**運営**する
- 自分が責任を持って**守る**

---

![bg left](https://images.unsplash.com/photo-1674049404913-2005c02245fa)

## 守れなかったら…

- 泥棒に入られる
- 何かを盗まれる
- 乗っ取られる
- 悪い人の拠点にされる
- **他の家に迷惑をかける**

---

## WordPress のセキュリティ対策とは

- 自身のウェブサイトの**情報を守る**ための取り組み
- 自身のウェブサイトが**他社に悪影響を及ぼさない**ための取り組み

---

<!--
_class: section-title
-->

# セキュリティ設定の基本

---

## 強力なパスワード

- 20文字以上
- 小文字と大文字を使用
- 数字を含む
- 特殊文字を含む `!"#$%&'()*+,-./:;<=>?@[]^_{}|~`
- 適切なパスワード例 : `As32!KoP43??@ZkI??L0d`

---

## 絶対に避けるべきパスワード

- パートナーや子供の名前
- ペットの名前
- 会社名
- 好きなスポーツチームや車の名前
- 生まれた年
- あなたの誕生日

これらはすべて公開情報→簡単に推測される

---

## WordPress で自動生成する

![bg]()

---

<!--
_class: section-title
-->

# アップデートの重要性

---

<!--
_class: section-title
-->

# 信頼できるプラグインの活用

---
<!--
_class: section-title
-->

# バックアップという保険

---

<!--
_class: section-title
-->

# ユーザー管理と権限設定

---

<!--
_class: section-title
-->

# セキュリティに対する意識向上

---

<!--
_class: section-title
-->

# 今日から始められるセキュリティ対策

---