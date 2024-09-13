---
theme: default
paginate: true
header: "安心してウェブサイトを運営するためのWordPressセキュリティの基礎知識"
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

# 安心してウェブサイトを運営するためのWordPressセキュリティの基礎知識

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

- 前提認識・知識
- WordPress セキュリティの考え方
- 入り口を固める
- WordPress 本体・テーマ・プラグインのアップデート
- 「アップデートしない」は無い
- バックアップという保険
- プラグインの活用
- ユーザー管理と権限設定
- セキュリティに対する意識向上
- まとめ

---

<!--
_class: section-title
-->

# 前提認識・知識

---

## 想定

- 一般的な WordPress の利用方法を想定
- WordPress.org（インストール型）を想定

---

## WordPress とは

- コンテンツマネージメントシステム（CMS）の１つ
- グローバルシェアは約43%
- [日本国内シェアは82%以上](https://w3techs.com/technologies/segmentation/cl-ja-/content_management)

---

## 一般の皆さんの利用方法例

- 独自ドメイン利用、レンタルサーバーで稼働
- 専門家ではない個人（社内web担当者含む）が管理、または専門家に委託

---

## システムであり、ソフトウェアである

- CMS:コンテンツを管理するシステム 
- "WordPress is open source software."
  - 引用：[About – WordPress.org](https://wordpress.org/about/)

---

<!--
_class: section-title
-->

# WordPress セキュリティの考え方

---

![bg left](https://images.unsplash.com/photo-1460408037948-b89a5e837b41)

## WordPress は自分の家

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

## なぜセキュリティ対策をするのか

- 自身のウェブサイトの**情報を守る**ため
- 自身のウェブサイトが**他に悪影響を及ぼさない**ため

---

## 対策対象は大きく分けて２つ

- 入り口（ログイン画面）
- WordPress 本体（コア）・テーマ・プラグイン

---

<!--
_class: section-title
-->

# 入り口を固める

---

## 一意のアカウント名

- ブルートフォース攻撃では一般的なユーザー名とパスワードの組み合わせ辞書を使用する
- `admin` は使わない
- ユーザー名は公開情報
- ユーザー名は推測されやすい

---

## 強力なパスワード

- 20文字以上
- 小文字と大文字を使用
- 数字を含む
- 特殊文字を含む `!"#$%&'()*+,-./:;<=>?@[]^_{}|~`
- 適切なパスワード例 : `As32!KoP43??@ZkI??L0d`

---

## 絶対に避けるべきパスワード

- パートナーや子供、ペットの名前
- 会社名
- 好きなスポーツチームや車の名前
- 生まれた年
- あなたの誕生日

これらはすべて**公開情報**→**簡単に推測される**

---

## WordPress で自動生成する

---

<!--
_class: only-bg-image
-->

![bg](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/basic-knowledge-of-wordpress-security-to-run-your-site/asstes/images/wp-password-generate.png)

---

## ブラウザのパスワードマネージャーを利用する

- Chrome, Safari, Firefox など主要ブラウザで利用可能
- パスワードを自動生成して保存をサポートしてくれる
- パスワードを覚える必要がない
- 共有する場合はアプリを利用する
  - [1Password など色々とある](https://en.wikipedia.org/wiki/List_of_password_managers)

---

![bg left](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/basic-knowledge-of-wordpress-security-to-run-your-site/asstes/images/securi-password-check.png)

## パスワードの強度チェック

- [How Secure Is My Password?](https://www.security.org/how-secure-is-my-password/)

---

## ２要素認証（2FA:Two-Factor Authentication）

２つの異なる要素を使って認証する（以下のうち２つを組み合わせる）

1. 知識要素（パスワードやPIN）
2. 所持要素（スマホなど）
3. 生体要素（指紋や顔認証）

---

<!--
_class: section-title
-->

# WordPress 本体・テーマ・プラグインのアップデート

---

## アップデートとは

- 機能の追加
- バグの修正など

**最適な状態を保つための取り組み**

---

![bg left](https://raw.githubusercontent.com/Olein-jp/slide/main/doc/basic-knowledge-of-wordpress-security-to-run-your-site/asstes/images/WordPress-update-sign.png)

## アップデート対象

- WordPress本体（コア）
- テーマ
- プラグイン

---

## コアアップデートの種類

| 種類 | 主な内容         | 頻度  | バージョン番号の変化 |
| --- |--------------|-----|-----------|
| メジャーアップデート | 新機能の追加、パフォーマンス向上など | 年に３回（2023年の事例）| 6.6 → 6.7 |
| マイナーアップデート | バグ修正、セキュリティ修正など | 不定期 | 6.6.1 → 6.6.2 |

---

## アップデートを躊躇する理由

- **画面が真っ白になるかも**しれない
- **エラーが出るかも**しれない
- **表示が崩れるかも**しれない

--

- これらの情報を見聞き（または体験して）して恐る

---

## アップデートをしなかったら？

- 脆弱性を抱えた状態で公開される可能性
- サイトが乗っ取られる可能性
- 踏み台にされる可能性（他への攻撃につながる）

---

## 僕がお勧めするアップデートに対する考え方は…

### アップデートは可能な限り早期に実施する

- 画面が真っ白になったら**対処する**
- エラーが出たら**対処する**
- 表示か崩れたら**対処する**

--

- 脆弱性を抱えて誰かに迷惑をかけてしまう or 表示が崩れる
- 見えにくい問題を抱える or 見える問題を抱える

どちらを選ぶ？

---

## 何かに対処することは運用の一部

- 日々の運用で改善を繰り返すのがウェブサイト運用
- 課題・問題→対処→効果測定などの繰り返し
- アップデートもその一貫だと考える

---

## アップデートで問題が起きにくい作りを考える

- WordPress への理解
- 見た目（テーマ）と機能（プラグイン）の分離
- 継続的メンテナンスができない機能追加は慎重に検討する

---

<!--
_class: section-title
-->

# 「アップデートしない」は無い

---

## テスト環境でアップデートを試す

1. 稼働ウェブサイトと全く同じものを壊れても良い環境に用意する
2. 実際にアップデートを行う
3. 管理画面や実際の表示に問題がないか確認する
4. 問題がなかったら or 問題を解決したら本番環境でアップデートを行う

---

## 自動アップデートを適切に活用する

例えば…

- WordPress マイナーアップデートは有効化する
- ユーザーから情報入力があるプラグインは有効化する
- 表示（フロント側）に影響がないプラグインは有効化する

などなど

---

## .。(「本業ではないので簡単に言わないでください」)

ウェブサイトの運用・運営は以下の３つに絞れる

- 自分で運用・運営する
- 専門家に委託する
- 適材適所で依頼・委託する

本業ではない方は、**困った時に相談できる専門家を見つけておく**と良いかも

---

<!--
_class: section-title
-->

# バックアップという保険

---

## バックアップは何か問題が起きた場合の重要な備え

- アップデートで問題が発生した場合に利用
- ハッキングされた場合のロールバックに利用
- その他、想定外の問題が発生した際に復元に利用

---

## バックアップ取得の頻度

- ウェブサイトにより最適解が変わる
- ウェブサイトの更新頻度によって最適解を探る必要がある

---

## バックアップ取得方法

- プラグインで行う（推奨）
  - [UpdraftPlus](https://ja.wordpress.org/plugins/updraftplus/)
  - [BackWPup](https://ja.wordpress.org/plugins/backwpup/)
  - [All-in-One WP Migration](https://ja.wordpress.org/plugins/all-in-one-wp-migration/) など
- 自身で手動で行う
  - データベースの書き出し
  - `/wp-content/` ディレクトリのコピーなど

---

意外と盲点！

## バックアップからの復元方法の確認

- バックアップを取得するだけでなく、復元方法も確認しておく
- いざという時はトラブルが発生している状態
- そんな時にも適切に対応できるように準備しておく

---

<!--
_class: section-title
-->

# プラグインの活用

---

## よく聞くセキュリティ系プラグイン

- [Wordfence](https://ja.wordpress.org/plugins/wordfence/)
- [Sucuri Security](https://ja.wordpress.org/plugins/sucuri-scanner/) 
- [XO Security](https://ja.wordpress.org/plugins/xo-security/)
- [SiteGuard WP Plugin](https://ja.wordpress.org/plugins/siteguard/)

などたくさんある

---

## セキュリティ系プラグイン利用について（個人的な意見）

- プラグインを**入れる前にやるべき対策がある**ことを理解
- それらが完璧に対応された上での利用を推奨する
  - ログイン周りが弱いと総合的なセキュリティレベルを上げられません

**「セキュリティ系プラグインを入れたから安心」という考え方は危険**

---

<!--
_class: section-title
-->

# サーバーのセキュリティ

---

## SSLの導入

- インターネット通信の暗号化するセキュリティ機能
- SSL 証明書は上記の情報暗号化通信に加え、そのウェブサイトが信頼できるものであることを証明する
- 多くのレンタルサーバーで無料で導入・設定が可能
- SEO の観点からもメリットがある

---

## サーバー内のファイル権限設定

- ファイルの読み書き権限を適切に設定する
- レンタルサーバーが用意する簡単 WordPress インストール機能を使っておけば問題ない

---

<!--
_class: section-title
-->

# ユーザー管理と権限設定

---

## ユーザーアカウントは一人に一つ

- ユーザーアカウントを複数人で共有しない
- 誰がいつどんな操作をしたのか特定できなくなる
- 一人がパスワードを変更した場合、他の人がログインできなくなる

---

## 必要最小限の権限を与える

- ユーザー毎に適切な権限を最小限で与える
- WordPress に詳しくない人には管理権限を普段使いさせない
  - 普段は最低限の権限を提供し、必要な場合のみ管理者権限を利用するなどの方法もあり

---

## ユーザーの活動監視

- 各ユーザーの WordPress 内での活動内容を記録・監視する
- 問題が発生した場合に、実行者の特定と以後の改善方法共有などが可能になる

--

- [Simple History](https://ja.wordpress.org/plugins/simple-history/)
- [WP Activity Log](https://ja.wordpress.org/plugins/wp-security-audit-log/)

---

<!--
_class: section-title
-->

# セキュリティに対する意識向上

---

## 対策実行とアップデートの大切さを知る

- 自身の環境と照らし合わせて、必要な対策を速やかに実施する
- アップデートの重要性を理解し、適切なタイミングで実施する

---

## セキュリティに関する情報を定期的にチェック

- 信頼できる情報源を見つける
- WordPress Meetup などのコミュニティに参加し情報収集する
- セキュリティに関する情報収集は立派な「保守」の一部

---

# まとめ

- WordPress セキュリティは自身の家を守ることと同じ
- 基本的な点をしっかり対策する
- アップデートは実施する前提で WordPress を使う
- 情報収集を継続的に行う

---

# おまけ

## 僕の基本セキュリティ対策

- パスワードを強固なものにする
- ログイン画面にひらがな画像認証を導入
- １時間におけるログイン試行回数制限
- 二要素認証の導入
- コメント機能の無効化
- WordPress コアはマイナーアップデート自動化
- テーマ・プラグインは可能な限り自動アップデート有効化
- バックアップは毎日取得し、稼働サーバーとは別の場所に保存

---

## 参考資料一覧

- [Password Best Practices](https://wordpress.org/documentation/article/password-best-practices/)
- [Updatiing WordPress](https://wordpress.org/documentation/article/updating-wordpress/)
- [Usage statistics and market share of WordPress](https://w3techs.com/technologies/details/cm-wordpress)
- [Changing File Permissions – Advanced Administration Handbook](https://developer.wordpress.org/advanced-administration/server/file-permissions/)
- [サイバーセキュリティ初心者のための三原則](https://www.soumu.go.jp/main_sosiki/cybersecurity/kokumin/intro/beginner/)
- [安全なパスワードの設定・管理 | 国民のためのサイバーセキュリティサイト](https://www.soumu.go.jp/main_sosiki/cybersecurity/kokumin/security/business/staff/06/)
- [インターネットの安全・安心ハンドブック - NISC](https://security-portal.nisc.go.jp/guidance/handbook.html)