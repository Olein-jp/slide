---
theme: default
paginate: true
footer: "WordPress の保守について" 
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

# WordPress の保守について

---

![bg left](https://olein-design.com/wp-content/uploads/2023/08/kuno_high-quality_square-768x768.jpg)

# 自己紹介

- 久野 晃司（岐阜県岐阜市在住）
- [オレインデザイン](https://olein-design.com)
- フリーランス ウェブ制作者
- [WordPress コントリビューター](https://profiles.wordpress.org/olein/)
- Snow Monkey エキスパート
- 最近は unitone 触ってます
- [hook wp_](https://hook-wp.com/) メンバー
- [本、書きました（TT4本）](https://amzn.to/4fKGPWd)

---

# アジェンダ

- 「保守」と「メンテナンス」の定義
- WordPress の保守で行うこと
- 保守に必要な費用
- なぜ保守が必要なのか
- まとめ

---

<!-- _class: section-title -->

# 「保守」と「メンテナンス」の定義

「保守」を翻訳すると「Maintenance」となる

---

# 「保守」とは

WordPress の全体的な機能を **長期間にわたり安定して稼動させるために必要な作業** を指す

- セキュリティ対策
- バックアップ取得と管理
- パフォーマンスの最適化
- 障害対応

---

# 「メンテナンス」とは

主に WordPress のコア、テーマ、プラグインのアップデートを含む **定期的な更新作業** を指す

- コアやプラグインのアップデート
- テーマの更新
- バグ修正

---

本セッションでは、ほぼ同義と考えて進めていきます。

---

<!-- _class: section-title -->

# WordPress の保守で行うこと

---

# 保守作業内容

- サイト死活監視
- コア・テーマ・プラグインのアップデート
- 定期的なバックアップ取得
- 緊急時のバックアップ復元
- テスト環境の構築
- 改ざんチェック
- サーバーに関するメンテナンスやアップデート
- パフォーマンスの最適化

---

# サイト死活監視

- ウェブサイトがアクセス可能かどうかをリアルタイムでチェックする
- サービスを利用 or 独自に通知システムを用意
  - Slack や Discord、chatwork に通知させると便利

---

# コア・テーマ・プラグインのアップデート

- WordPress のコア・テーマ・プラグインのアップデートを定期的に行う
- 頻度や自動設定なプロジェクトによって異なる

---

# 定期的なバックアップ取得

- ウェブサイトのデータを定期的にバックアップする
- 安全な場所に確保することを推奨

---

# 緊急時のバックアップ復元

- ウェブサイトがダウンした際に、バックアップから復元する
- 事前に復元手順を確認しておく
  - テスト環境での復元を練習しておくとよい

---

# テスト環境の構築

- 大きなアップデートを実施する前にテスト環境で確認する
- ローカル環境、またはサブドメイン利用にて稼動サーバーと同じ環境を用意する
- ビジュアルリグレッションテストを行うと表示崩れを確認しやすい

---

# 改ざんチェック

- Wordfence などセキュリティプラグインを利用して確認する
  - 参照：[Wordfence](https://wordpress.org/plugins/wordfence/)
- WPScan などのツールを利用して確認する
  - 参照：[WPScan](https://wpscan.com/)

---

# サーバーに関するメンテナンスやアップデート

- レンタルサーバーの場合は特に行うことはない
- PHP や MySQL のバージョンは利用する WordPress に最適なものを採用する
  - 参照：[PHP Compatibility and WordPress Versions](https://make.wordpress.org/core/handbook/references/php-compatibility-and-wordpress-versions/)

---

# パフォーマンスの最適化

- ウェブサイトの表示速度が遅くならないようにする
- SEOにも関係してくる可能性がある

---

<!-- _class: section-title -->

# 保守に必要な費用

---

# 相場感

- 月額5,000円〜30,000円程度（個人の感覚です）
- 保守作業内容によって異なる

---

# 考え方

1. 自分で行えるかどうか
2. 自分で対応できない部分は委託する
3. すべて委託する

---

<!-- _class: section-title -->

# なぜ保守が必要なのか

---

# WordPress はシステムでありソフトウェアである

- "WordPress is open source software."
    - 引用：[About – WordPress.org](https://wordpress.org/about/)

---

# アップデートしない（されない）システムは脆弱化する

- 世界は絶え間なく変化している
- インターネットの世界も同じ
- それに合わせて随時アップデートされている
- **「実施しないこと」は「意図的にシステムを脆弱化する」こと** になる

---

# コア・テーマ・プラグインにアップデートが用意されるから

- アップデートは「より良い状態にするもの」

## 主な内容

- セキュリティの強化
- バグ修正
- 新しい機能追加など

---

# トラブルに備えるため

- WooCommerce などを利用して EC 機能を有している場合
  - 利用者情報（個人データ）やカード情報・購入履歴などを保護する
  - 参照：[プライバシーマーク制度](https://privacymark.jp/p-application/new/index.html)
- サイトがダウンした際の対応策を用意しておく

---

# 閲覧者のため

- ウェブサイト表示速度を最適化することで閲覧者の体験を向上させる
  - SEO にも影響する可能性がある（検索流入にも影響？）
- ウェブサイトがダウンしていると閲覧者は離れていく
- 閲覧者にとっては **「ウェブサイトは常に最適な状態で稼働していること」が普通** になっている

---

<!-- _class: section-title -->

# まとめ

---

- 「保守・メンテナンスをしない」はない
  - しないならシステムを使わない方法も検討すると良い
- 保守には費用がかかる
  - 自分で行う（学習コスト等必要）
  - 委託する（費用がかかる）
- 閲覧者（お客さん）のためでもある

---

# ご清聴ありがとうございました

WordPress の面倒をちゃんとみながら、楽しいウェブサイト運営をしていきましょう！