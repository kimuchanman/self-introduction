# 職務経歴書

## 基本情報

|key|value|
|:---:|:---:|
|氏名|木村 慶 (Kimura Kei)|
|生年月日|1995/08/11|
|GitHub|[GitHub](https://github.com/kimuchanman)|
|Qiita|[Qiita](https://qiita.com/kimuchan)|
|SpeakerDeck|[SpeakerDeck](https://speakerdeck.com/kimuchanman)|

---

## 理念

プロダクトの価値をより加速させやすい環境を創造し、私の携わったプロダクトをもっと成長させられる存在でありたい。

## 保有スキル

- システム設計から実装まで
- 割と幅広く
    - JavaScript / TypeScript + Vue.js(Nuxt.js) でのフロントエンド実装から
    - Ruby on Rails / CakePHP / Laravel でのバックエンド実装から
    - RDB 設計やパフォーマンスチューニング
    - を適切に AWS を利用（2019 年に Solution Architect Association 取得済みです）しつつ行うことができます
    - 耐障害性や SPoF をなくすシステム設計を考えるのが好きだったりします
- また、アジャイル、スクラムの進行補助やプロジェクトマネジメントの経験もあります
- paiza はシステムの都合上 public にプロフィールを公開できないですが S ランク です
- E2E テストの保守運用

---

## 技術スタック

### 言語

- PHP / TypeScript / Ruby / Go / Haskell

### フレームワーク・その他

- CakePHP / Ruby on Rails / Laravel / Vue.js(Nuxt.js)
- PHPUnit / RSpec / Jest / Selenium WebDriver や Cypress を用いた E2E テスト
- AWS は Solution Architect Associate(SAA) を取得しています。基本的なサービスはだいたい業務や個人で触っています

---

## 職務経歴概略

### BASE株式会社（2020/08〜現在）

#### インスタ広告 App の開発

BASE にて[こちら](https://admin.thebase.in/apps/110)の App の開発を行いました。
こちらは、Facebook Marketing API を使った外部連携機能です。
API ドキュメントにはたまに正しいことが書かれていなかったり、連携先の環境は本番としか繋げられないがショップアカウントの開設条件が厳しいかったり、外部連携ならではの開発以外のところでの苦労が多かったです。

#### 顧客管理システムの開発とリアーキテクト
- こちらのブログを執筆しました
- [BASEの顧客管理はどのようにして実現されたか](https://devblog.thebase.in/entry/2021/12/02/110000)
- また、こちらの YouTube にてインタビューしていただきました
    - [https://youtu.be/JE9bncvlc8c](https://youtu.be/JE9bncvlc8c)
    - <iframe width="560" height="315" src="https://www.youtube.com/embed/JE9bncvlc8c" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    - [https://youtu.be/u-BD28cGH98](https://youtu.be/u-BD28cGH98)
    - <iframe width="560" height="315" src="https://www.youtube.com/embed/u-BD28cGH98" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
- CakePHP, 各種 AWS サービス（SNS と SQS を用いた非同期化など）
- 非同期アーキテクチャ、イベント駆動設計、マイクロサービス化

### 株式会社LIFULL（2018/04〜2020/07）

#### サイトリニューアルに向けた大規模リファクタリング
- Ruby on Rails 5.1
- Docker
- AWS(ECS,CodePipeline,Route 53, ALB)
- nginx
- Webpack
- Vue.js
- vue-property-decorator
- TypeScript

```
自社のサイトで

- ドメイン変更
- サイト名変更
- 全体のデザイン変更

などを含めたの大幅なリニューアルがありました。

私はこのプロジェクトに最初から関わり、主に開発メンバーとして参画しました。
上で挙げたリニューアルの観点とは直接的には関係しませんが、そのそもそのサービスの前身が2016年ごろにかなりスピード重視で開発されたもので当時スピーディに開発する選択肢としてRailsを選択した経緯があり、今後手を加えていくのがかなりキツイ現状でした。

そのため、私含め開発メンバー4人でリファクタリングを同時に進めていきました。

まず、携わっていたサービスはほとんどのデータのやりとりがAPIを介して行われていたため、Virtusをいうgemを用いて、オブジェクトのattributeを型定義し、APIを介して取得されたオブジェクトとAPIを見える化しました。アプリケーション規模も大きくなっていたのでRails wayから離れリポジトリパターンを導入し、上記のVirtusを用いてEntityをしっかり型定義し、リポジトリ層Service層と責務をしっかり明記することでアプリケーションの見通しを良くしました。

さらに、基盤をコンテナ化しECSに乗せる上でデプロイ手法もOpsWorksからCodePipelineに切り替えました。

また、webpackも導入し一部フロントもVue.jsを取り入れ、新規のjsファイルはどんどんTypeScriptで作成していけるようにしました。Vue.jsを取り入れたものの、SEOの観点でSSRが求められるケースが多く、まだjQueryで実装が余儀なくされることが多いので、フロントのNuxt.js移行が今後の課題に挙げられます。

また、サイトリニューアルに伴って、影響範囲が全てのページにあたり、TDK、OGP、DataLayer、Json-LDに挙げられるmetaタグ内のコンテンツも全て新規のものになりました。それらのテストのために、以前から採用していたE2Eテストも大幅に変更を加え、保守しました。その結果、サイトリニューアル時のテストはほとんど自動テストに任せれば良くなりデグレの早期発見や不安も取り除かれ、チームの開発効率が向上しました。

以上に挙げたほとんど全てに私も携わり、中でもE2Eテストの保守は私1人で行いました。
```

#### 地域情報に関連する記事更新の自動化
- MeCab
- Ruby 2.4
- AWS(EC2, CloudWatch, ElastiCache for Redis, VPC ピアリング、 AssumeRole)

```
自分が携わっているサイトの都道府県のLP（ランディングページ）で、その都道府県に関連した記事を表示するというものをやりました。

以前は手作業かつ、1都3県のみ対応のサイトだったため記事は全て同じものを表示させていました。

サイトを全国化させていく中で、手作業は無理だしそれぞれのLPで記事を最適化させたいという要件が出ました。

そこで、私が提供元のサイトから記事を抽出し、mecabを用いて記事を形態素解析し記事に対してそれぞれ都道府県への関連度を重み付けし関連記事として判定＆Redisに格納するバッチを作成し自動化させました。

「関連度」という抽象的なもののアプローチとしては形態素解析などの自然言語のアプローチ無くしては不可能だろうと考え、mecabも触るのは初めてでしたが、ドキュメントや内部のコードを読み解きなんとかものにしてリリースできました。mecabの環境構築の際に標準の辞書データのインストールするのに2GB以上のメモリ容量が必要で使用が許されたEC2インスタンスがt2.smallまでだったらめ標準辞書だとインストールにギリギリ失敗していたので、分析に用いる辞書データを限定的に入れることで解消しました。

このプロジェクトは2018年12月〜2019年2月で完全に私1人で開発しました。

同時に今回、バッチが動かすAWSアカウントと記事データを格納するDBを所有するAWSアカウントが異なることから、問題解決のためのAWSの知見もかなり深まりました。

記事データを異なるAWSアカウントのS3とRedisに格納する必要があり、S3はassume roleを活用し、RedisはVPCピアリング接続して解決しました。

また、バッチの自動化のためCloudWatch Events、サービスオーナーへの通知にAWS SNSを活用しました。

このプロジェクトを完遂するまではAWSにあまり詳しくなかったのですが、本プロジェクトを通してかなりAWSのノウハウがたまりましたのでAWS Solution Associate認定試験を後日受験し、見事合格しました。
```

#### E2Eテストの保守/運用
- Selenium
- WebDriver
- Mocha.js

```
私が携わっているサイトの保守運用のためのE2Eテストを管理していました。

mocha.jsというライブラリを利用しSelenium WebDriverを動かしています。

yamlでmocha.jsの書式で書かれたものを展開してテストを実行するという手法を取っていますが、その仕組みは社内の独自のライブラリを使っているため、Seleniumのバージョンが依存していてなかなか上げられていません。
そのため、まだSelenium WebDriverのヘッドレス化かできておらずCI/CDに組み込めていないなどの課題感を感じていますが、サイトの大幅リニューアルなどもありE2Eテストを保守するので手一杯で改善に手が回っていませんでした。。

保守とテストの管理を行う中で工夫していたことは、SeleniumもといE2Eテストに明るくない開発者が如何にテストコードに手を入れやすくするかです。サイトの開発者がDOMやセレクタを変えたら、その人が該当のE2Eテストの箇所を改修できるようにドキュメントをまとめたり、コードを使いやすく抽象的にカプセル化し感覚で使えるよう修正していきました。

困難だったことは、やはりE2Eテストを1人で片手間で管理することでした。
E2Eテストの保守と運用は知られている通りなかなかに骨の折れるもので、社内のメインサービスのE2Eテストでは専用のチームがあるくらいです。私が携わっているサイトはまだ発展途上のもので日々変更があるため保守の大変さに拍車をかけますが、チームでSeleniumに知見があるのが少ないためほぼ1人で管理していました。
また、Seleniumの知見が全くないメンバーだと簡単なE2Eテストの追加や修正でも時間がかかってしまうということに課題感を感じ、Seleniumの公式ドキュメントから、よく使うWebElement系の操作やWebDriverの待ち動作（until系）のコードをメンバーに共有し、よくあるE2Eテストの追加や修正の例を示すことで他のメンバーによるテストコードの実装が比較的簡単になり負担を分散させることができました。

とはいえ、私も2018年の冬にE2Eテストの社内ツールを触るまでSeleniumの知見はなく、そこからサイトの開発の片手間にキャッチアップしていきました。今では自サイトのE2Eテストの管理者として保守とテストの管理をしています。
```

### 株式会社NoSchool（2019/04〜2020/04）

#### WordPressで運用していたサイトのリプレイス（Laravel & Nuxt & AWS移行）

```
副業先の教育×テクノロジーの分野でプロダクトを展開しているところで、脱WordPressをしていました。

Laravelを用いて1次のリプレイスは進めていたものの、フルでLaravelはフロントが辛いということもありLaravelでどんどんAPIを作りNuxt.jsにフロントをリプレイスしていました。

そこで、私は管理画面系のLaravel & Nuxt.jsのリプレイスとAWSの知見を生かしてデプロイやVPCの構築やRoute 53やALB周りの顧問的な立場も任されました。

Laravelでリポジトリパターンを採用しました。admin用のmiddlewareをLaravel, Nuxtともに作成し、Redisでセッション管理してLaravel, Nuxt両方からログインユーザの整合性の問題も解消しました。Laravelのコントローラまでに権限周りのバリデーションを集約し、サービス層にユースケース集約しResouceでレスポンスをラッピングしてどんどんAPI作っていきました。
Nuxtでフロントを開発していく際、メインで作成していったのは管理画面系で、それは内部の人が使うものなので、デザインは手早く組めるものを使用したく、Vuetifyを導入しました。
管理画面系は情報の網羅性が求められるためv-data-tableはよく用いました。v-data-tableは多くのslotを用意しておりslotの宝庫なので、v-data-tableをどんどんカスタマイズしていく中でVuetifyの内部実装を見にいくことが多く、OSSとして高度に抽象化されたコンポーネント設計を見ながら、何をPropsに持つべきか、どこをslot化させるべきか、など学びも多くエキサイティングでした。
Vuetifyの使用感はとてもよく、Vueのコンポーネント思想とUIフレームワークはとても相性が良いことを実感しました。

Vuetifyを使い倒して知見も溜まったので、Vuetify_meetupというイベントにも参加して登壇しました。
こちらがその時の登壇資料です。
https://speakerdeck.com/kimuchanman/fei-hurontoensiniakabao-su-tevuetifywoshi-utamenikiyatutisita6tufalsekoto

また、API開発の際に、LaravelのJsonResourceとTypeScriptではaspidaというHTTP クライアントラッパーのOSSを活用しました。
JsonResourceを用いることで、Laravel側のAPIレスポンスを最適化しなおかつ見える化しました。
aspidaを用いることでNuxt.js側でもAPIが見える化され、なおかつTypeScriptの推論の恩恵を大きく得られました。知り合いがaspidaの開発者なのも大きいのですが、aspidaは個人的にも応援しているOSSの一つで、以前紹介記事をQiitaに書かせていただきました。
https://qiita.com/kimuchan/items/c60fbcb8e71baace0fc6
```

### LIRIS（ライリス）株式会社（2019/12〜2021/02）

#### 契約ライフサイクルマネジメントサービスの開発

[こちら](https://clmlp.liris.co.jp/)のサービスの主にフロントエンド部分（Vue.js）の開発をしていました。</br>
アトミックデザインに沿ったコンポーネント設計指針の元開発していました。
Cypress で Vue,js の E2E テストも書いていました。

## 業務外活動

- Vuetify_meetup
    - 登壇しました
    - [非フロントエンジニアが爆速でVuetifyを使うためにキャッチした6つのこと](https://speakerdeck.com/kimuchanman/fei-hurontoensiniakabao-su-tevuetifywoshi-utamenikiyatutisita6tufalsekoto)
- aspida
    - early adaptor として導入記事書かせていただきました
    - [aspidaでフロントエンドからAPIを見える化する](https://qiita.com/kimuchan/items/c60fbcb8e71baace0fc6)

---

## パーソナル

サウナが好きで、週 7 で行ってます！
