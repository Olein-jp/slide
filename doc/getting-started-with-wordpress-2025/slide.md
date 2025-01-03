---
theme: default
paginate: true
footer: "これからはじめるWordPress" 
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

# これからはじめる WordPress

---

![bg left](https://olein-design.com/wp-content/uploads/2023/08/kuno_high-quality_square-768x768.jpg)

# 自己紹介

- 久野 晃司（岐阜県岐阜市在住）
- フリーランス ウェブ制作者
- [オレインデザイン](https://olein-design.com) 代表
- [WordPress コントリビューター](https://profiles.wordpress.org/olein/)
- Snow Monkey エキスパート／最近は unitone 触ってます
- [hook wp_](https://hook-wp.com/) メンバー
- 岐阜市登録市民団体 Shift 代表

---

![bg left contain](https://olein-design.com/wp-content/uploads/2024/12/tt5-book-hyoushi.jpg)

# 新刊紹介

## 『Twenty Twenty-Fiveでウェブサイトを作ろう』

Amazon Kindle で発売中。Kindle Unlimited で無料で読めます。

- 2024.12.13 発売開始
- 2025.01.02 英語版リリース

---

# 前提

- WordPress.org の WordPress を利用する前提で話を進めます
- WordPress.com には触れません
- 内容は個人の見解です

---

# アジェンダ

- WordPress とは
- WordPress の強みと弱み
- 始める前に知っておきたいこと
- 最低限知っておきたい知識と設定
- ウェブサイト運営とは

---

<!-- _class: section-title -->

# WordPress とは

---

## WordPress とは

- オープンソースの CMS（コンテンツ管理システム）
- 世界で43%以上のウェブサイトで利用されている
- 日本国内での CMS シェアは 80% 以上
- 無料で利用可能

---

## オープンソースとは

- ソースコードを一般公開すること
- 誰でもソフトウェアの開発に参加できる
- 世界中に貢献者がいて、開発が進められている

---

## GPL というライセンスとは

- General Public License の略
- WordPress は GPL ライセンス

--

1. あらゆる目的でプログラムを実行する自由
2. 変更する自由
3. 再配布の自由
4. 改変し頒布する自由

---

## コミュニティ

- 国内には 26 の WordPress Meetup グループが活動している（2024年11月現在）
- 対面・オンラインでの勉強会や交流会が開催されている
- WordPress ダッシュボードのウィジェットで近くのイベントを確認可能
- WordCamp という大きなイベントも開催される

---

<!-- _class: section-title -->

# WordPress の強みと弱み

---

## 強み

- 豊富なテーマとプラグインが利用可能
- シェアが高いので情報が豊富
- コンテンツを自分で保持・管理できる

---

## 弱み

- サーバー費用などが必要になる
- すべてを自分で管理しなくてはならない
- 頻繁にアップデートが実施され、最新情報を自ら追いかけるのが大変な場合がある
- 情報は多いが古いものも多い

---

<!-- _class: section-title -->

# 始める前に知っておきたいこと

---

## WordPress を選ぶ理由

- なぜ WordPress を選択するのか
  - WordPress でなければならない理由は？
  - WordPress 以外の選択肢を考えた？
- **システムを運用する**ということを考えた？

---

## なぜウェブサイトが必要なのか

- ウェブサイトを持った先に達成したいゴールを持つこと
- ゴールを持たないウェブサイトの多くは放置される
  - あるだけで良いウェブサイトもあるのでそれは除く

---

## 環境

- サーバー
    - 最初は手軽なレンタルサーバーで十分
    - SAKURA Internet/スタンダード：¥500〜/月
    - XServer/スタンダード：¥693〜/月
- ドメイン（なくても良い）
    - さくらのドメイン
    - XServer 独自ドメイン永久無料特典 有り

---

## テーマについて

- これから始めるなら**ブロックエディターに対応したテーマ**を選ぶことを推奨
- **ブロックテーマ** or **クラシックテーマ** どっちを選ぶ？
  - WordPress の最新機能に触れていきたいなら**ブロックテーマ**
  - 素早く立ち上げたいなら**クラシックテーマ**

---

## プラグインについて

- 日本語サイトなら**WP Multibyte Patch**は必須
- 必要ないものは入れない
  - どう機能するか把握できないものは入れない
- 「ブログ記事などで紹介されているから入れる」という安易な発想はやめよう
  - そのブログ記事はあなたのニーズを理解していない可能性も

---

## セキュリティについて

- 一意の ID とセキュアなパスワードは必須
- 画像認証など活用も良し
- ２要素認証の導入を推奨

---

## バックアップについて

- 万が一の場合に備えるためにバックアップを**取得**する
- 自分で復元できるようになると安心できるようになる
- 最悪**取得**していれば有識者に復元を依頼できる
- **取得**していなければそれまでのコンテンツを失う可能性もある

---

## アップデートについて

- WordPress 本体
  - 近年、年に3回のメジャーアップデートが提供される
  - その他に適時マイナーアップデートが提供される
- 利用するテーマやプラグインにも随時アップデートが提供される

--

- 「アップデートしない」は**ない**
- 「アップデートしない」なら「システムを使わない」方向で考える
- **どのタイミングでアップデートを実施するか**を考える

---

<!-- _class: section-title -->

# 最低限知っておきたい設定

---

![bg left contain](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/getting-started-with-wordpress-2025/assets/images/gsww-01.png)

## パーマリンク設定は慎重に

- 運営開始後に変更するとリダイレクト処理が必要になる

---

## 

---

# ウェブサイト運営とは

---