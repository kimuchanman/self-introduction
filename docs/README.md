# 職務経歴書

## 基本情報

|     key     |                       value                        |
|:-----------:|:--------------------------------------------------:|
|     氏名      |                 木村 慶 (Kimura Kei)                  |
|    生年月日     |                     1995/08/11                     |
|   GitHub    |      [GitHub](https://github.com/kimuchanman)      |
|    Zenn     |         [Zenn](https://zenn.dev/kimuchan)          |
|    Qiita    |        [Qiita](https://qiita.com/kimuchan)         |
| SpeakerDeck | [SpeakerDeck](https://speakerdeck.com/kimuchanman) |

---

## 理念

**プロダクトと組織のスケールに大きく寄与できる存在でありたい**

```
すべての行動はプロダクトのためでありたい。
そしてコンウェイの法則的にプロダクトの構造は組織構造と似てくる。
そのため、プロダクトをスケールさせることは組織をスケールさせることに似てくる。

ものづくりをする人として己の価値をどこに置くのか考えた時に、プロダクト（組織）をいわゆる1->100型の成長をさせるのが自分自身として得意だと感じています。
また、個人としてはその領域の興味がとても強いので特化したいと思っています。
```

**ユーザー体験の向上を追い求めたい**

```
ここで言うユーザーとは、社内の開発者も含めた全ての関係者を指します。
何よりも価値として尊いものはユーザー体験であると考えていますし、プロダクト観点でもユーザー体験が最もカネになるとも言われています。
社内などのインターナルな組織においてもそれは言えると思っていて、たとえば開発者体験の向上は開発者の離職率の低下に大きく寄与すると思っていますし、自分自身これまで色々やってきて重要視するものはやっていて気持ちいいかどうかだなーと感じ始めてきました。

これは私の行動指針にも大きく関わり始めています。なにかしらの選択肢があればどちらがより気持ちいい、楽しいか（体験が良いか）で個人的な決断をすることも増えてきました。
```

## 保有スキル

- システム設計から実装まで
- 最近はシステム設計を通した組織設計にも手を広げてきました
- 技術選定や導入から始まり、汎用的に使えるソリューションを提供し、委譲していくことで自分がいなくても回るようにするサイクルのやり方が人よりちょっと得意です
- 割と幅広く
    - JavaScript / TypeScript + Vue.js(Nuxt.js) / React(Next.js) / NestJS でのフロントエンドやミドルウェア実装から
    - Ruby on Rails / CakePHP / Laravel / Spring Boot でのバックエンド実装から
    - Auth0 と連携したシステム構築経験があります
    - RDB 設計やパフォーマンスチューニングを適切に AWS を利用（2019 年に Solution Architect Association 取得済みです）しつつ行うことができます
    - AWS OpenSearch Service で耐障害性を加味したインフラ環境の構築とドキュメント/インデックス構築の経験があります
    - 耐障害性や SPoF をなくすシステム設計を考えるのが好きだったりします
- また、アジャイル、スクラムの進行補助やプロジェクトマネジメントの経験もあります
- paiza はシステムの都合上 public にプロフィールを公開できないですが S ランク です
- E2E テストの保守運用

---

## 技術スタック

### 言語

- PHP / TypeScript / JavaScript / Ruby / Go / Haskell / Kotlin / Java

### フレームワーク・その他

- CakePHP / Ruby on Rails / Laravel / Vue.js(Nuxt.js) / React(Next.js) / Spring Boot / NestJS
- PHPUnit / JUnit / RSpec / Jest / reg-cli / textlint / Selenium WebDriver や Cypress を用いた E2E テスト
- Storybook / Chromatic
- Figma / yagisan-reports
- GraphQL (Apollo) / REST API
- Docker / Docker Compose
- GitHub Actions
- Auth0
- LaunchDarkly
- Terraform
- LocalStack
- MySQL / PostgresQL / DynamoDB / Redis / OpenSearch / Neon
- AWS は Solution Architect Associate(SAA) を取得しています。基本的なサービスはだいたい業務や個人で触っています。レアなスキルですと、 AWS OpenSearch Service の VPC 内とパブリックドメイン両方のインフラ環境の構築とドキュメント/インデックス構築の経験があります
- Miro / Jira / Notion

---

## 職務経歴概略

### 株式会社エス・エム・エス（2022/09〜現在）

プロダクト開発部 介護経営支援 開発グループ にて、[カイポケリニューアル](https://careers.bm-sms.co.jp/engineer/kaipoke-renewal)に従事。

#### 2024/10〜現在

##### 開発推進チーム


カイポケリニューアルの開発推進チームを発足&所属し、チームトポロジー文脈で言うところの platform engineering に近い立ち位置で、Stream-aligned チームの「開発効率」と「開発者の体験（Developer Experience, DX）」を向上することを目指して活動しています。

以下が主要な取り組みです。

  - Visual Regression Testing（VRT）基盤の大幅刷新
    - Chromatic のコスト課題を解決するため、Storycap + reg-cli ベースの VRT システムに移行
    - 1000 枚程度の Modal など動きのある画面や yagisan-reports を使った PDF レンダリングを含む画面の VRT と Storybook の配信を 5 分程度で実現
    - AWS CodeBuild の Large Runner を活用したパフォーマンスチューニング
    - VRT ワークフローの Composite Action 化による CI/CD の効率化と保守性向上
    - Datadog を活用した VRT メトリクスの可視化と監視基盤の構築
    - S3 + CloudFront による Storybook 配信基盤への移行で安定性向上
    - Flaky テストの自動検知・レポート機能の実装
    - Playwright ベースの VRT への移行によるスクリーンショット取得の高速化と安定性向上
    - VRT スクリプトのルートディレクトリ統合による保守性の向上
    - デザインサンドボックス（Ladle）の S3 アップロードと PR プレビュー機能の実装
    - これについて書いた blog: https://tech.bm-sms.co.jp/entry/2025/05/13/110000
  - Feature Flag 基盤の強化
    - Permission Toggle の導入および LaunchDarkly の組織全体への展開
    - 機能のロールアウト戦略とリスク管理の仕組み構築
  - CI/CD ワークフローの最適化
    - GitHub Actions の Composite Action を活用した DRY 原則の適用
    - VRT ワークフローの共通化により保守性とパフォーマンスを向上
    - Node.js 22 系への対応とビルドパフォーマンスの改善
    - CI ランナーの最適化によるコスト削減（Ubuntu-slim への移行など）
    - Prettier 自動修正・コミット機能の実装による開発フローの効率化
    - Renovate の設定最適化と週次自動更新ワークフローの構築
  - コード品質と DX 向上
    - 循環依存の自動検出・管理システムの運用改善
    - 日本語ファイル名の英語化によるプロジェクトの国際化対応
    - OSS ライセンス管理の自動化
    - ESLint によるクロスサービスインポート制限の導入（ドメイン境界の明確化）
    - 絶対パスインポート禁止ルールによるコードの保守性向上
  - pnpm workspace 導入による frontend のモノレポ最適化
    - パッケージ/アプリケーション分離に伴う各種設定や CI/CD の設計・実装
    - pnpm v10 への major upgrade と段階的な移行戦略の実行
    - pnpm catalogs での one version rule の実現と strict mode 化
    - 共通パッケージの構築と段階的なコンポーネント移行（500+ ファイル）
    - 複数ミニアプリの分離による開発効率とデプロイ速度の向上
    - カタログモードの strict 化による依存関係の厳密な管理
  - アーキテクチャとナビゲーション基盤の改善
    - ミニアプリ間のソフト/ハードナビゲーションを実現するルーティングマネージャーの設計・実装
    - navigation パッケージの新規開発による型安全なルーティング基盤の構築
    - pathpida からの移行と静的パス生成機能の実装
    - アプリ間遷移の自動判定機能（automatic navigation type）の導入
    - 認証・認可フローのリファクタリングによるテスタビリティと保守性の向上
    - テストダブル（Mock/Stub）の適切な活用によるテスト品質の改善
  - デザインシステムとコンポーネント基盤の強化
    - Link/Flex コンポーネントの次世代 UI ライブラリへの移行推進
    - asChild パターンの導入によるコンポーネントの柔軟性向上
    - recipe パターンを活用したスタイル定義の最適化
    - 複数アプリケーションへのコンポーネント移行とテスト整備
  - AI/自動化ツールの導入と生産性向上
    - Claude AI を活用したコードレビューワークフローの構築
    - 技術ドキュメント自動更新ワークフローの実装
    - Model Context Protocol（MCP）サーバーの開発・運用による開発体験の向上
    - Figma MCP サーバーの GitHub Packages 公開による社内配布の効率化
    - Figma デザインデータの自動取得・管理システムの構築
    - Claude Code 用カスタムコマンドの開発（スプリントレポート生成、議事録連携など）
  - その他の開発基盤改善
    - Datadog ソースマップアップロード処理の自動化と DRY 化
    - textlint による技術ドキュメントの品質向上と ADR 運用の推進
    - Storybook の改善と複数パッケージ間の統合
    - 複数アプリケーションの一括ビルド・プレビュー機能の実装
    - DateInput コンポーネントへの日付貼り付け機能追加による UX 向上
    - テストフレームワークの Jest から Vitest への移行推進
    - CODEOWNERS の整備によるレビュー効率化

以下がおもに利用した技術スタックです。
  - VRT: Playwright + reg-cli（Chromatic → Storycap → Playwright と移行）
  - Testing: Vitest（Jest から移行推進中）
  - Feature Flag: LaunchDarkly
  - CI/CD: GitHub Actions（Composite Action による共通化）
  - frontend: Next.js, pnpm v10, Turborepo
  - 監視： Datadog
  - AI: Claude Code, MCP（Figma MCP など）
  - ナビゲーション: navigation パッケージ（自社開発）

これらの活動により、開発チーム全体の生産性向上とコスト削減を同時に実現しました。月次で数十万円規模のインフラコスト削減に貢献しました。また、VRT の安定性向上により開発者の待ち時間を大幅に削減し、CI/CD パイプラインの信頼性を向上させました。
  
#### 2024/04 〜 2024/09

居宅支援チームに所属しつつ、技術戦略チームの発足に伴い、技術戦略チームにも所属しています（居宅支援チームでの開発も引き続き行っています）。

##### 居宅支援チーム

プロダクトの帳票出力機能に大きく課題があり、他社ツールやライブラリを含めた帳票出力の技術選定を行い、yagisan-reports を導入しました。
介護の帳票類は構成が複雑なものも多いですが、テンプレート作りやデータマッピングのやり方などを実際に作ったりサンプルを通してチームの誰でも書けるようにして委譲できる担当者を増やしていきました。

##### 技術戦略チーム

カイポケリニューアルは、プロジェクト規模や関係するチームが多岐に渡り長期的な目線を必要としている背景があります。

そのため技術戦略チームでは、プロダクトロードマップ・事業計画に対して Dev チームが、どこに・どのように投資をしていくかについての戦略と計画を立て不確実性の高い状態においてもチーム横断的な意思決定がしやすい状態を維持することを目的に活動しています。

私はまず組織に Architecture Decision Record（ADR）のテンプレートや文化の導入をもたらしたり、組織で汎用的に利用できるソリューションとしての非同期アーキテクチャの導入を行っています。
以降は、全 ADR のレビューを行っています（私から書くことももちろんあります！）。テクニカルライティング部分は人間のリソースは割かず textlint で調整しています。

その辺の話はテックブログ [ADRはじめました](https://tech.bm-sms.co.jp/entry/2024/07/23/110000) でまとめていますので、興味があればご覧ください。

#### 2023/10〜2024/03

居宅支援チームにて事業所管理ドメイン、ケアマネジメントドメイン、サービス提供管理ドメインのバックエンド開発をメインに行っている。
介護の請求が絡む部分で、めちゃくちゃ複雑なドメインにどう境界線を引いてどうコードで表現すると今後の法改正だったり機能の変更がしやすいかというのが主な考えごとになっている。

- Kotlin / Spring Boot
- PostgreSQL
- GraphQL / Apollo
- AWS
- GitHub Actions

#### 2022/09〜2023/09

プラットフォームチームにて、
カイポケ全体にわたる機能（アカウント（認証/認可）、コミュニケーション、販売管理）を開発した。
また、カイポケリニューアルのモノレポ化や全体の CI/CD の構築を行いました。
そのあたりの話は[ファーストリリース前にモノレポ移行した話](https://zenn.dev/kimuchan/articles/f5ba954ca4fbf8)でまとめています。

- Kotlin / Spring Boot
- PostgreSQL
- GraphQL / Apollo
- NestJS / Express.js
- Auth0
- React(Next.js)
- AWS
- GitHub Actions



### BASE株式会社（2020/08〜2022/08）

入社時のインタビュー記事です<br>
[https://basebook.binc.jp/entry/2020/08/31/180000](https://basebook.binc.jp/entry/2020/08/31/180000)

#### インスタ広告 App の開発

BASE にて[インスタ広告 App](https://admin.thebase.in/apps/110)の開発を行いました。
こちらは、Facebook Marketing API を使った外部連携機能です。
API ドキュメントにはたまに正しいことが書かれていなかったり、連携先の環境は本番としか繋げられないがショップアカウントの開設条件が厳しいかったり、外部連携ならではの開発以外のところでの苦労が多かったです。

#### 顧客管理システムの開発とリアーキテクチャ
- 詳しくは、執筆しましたこちらのブログをご覧いただければ幸いです
    - [BASEの顧客管理はどのようにして実現されたか](https://devblog.thebase.in/entry/2021/12/02/110000)
- また、こちらの YouTube にてインタビューしていただきました
    - [https://youtu.be/JE9bncvlc8c](https://youtu.be/JE9bncvlc8c)
    - <iframe width="560" height="315" src="https://www.youtube.com/embed/JE9bncvlc8c" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    - [https://youtu.be/u-BD28cGH98](https://youtu.be/u-BD28cGH98)
    - <iframe width="560" height="315" src="https://www.youtube.com/embed/u-BD28cGH98" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
- CakePHP
- Amazon SNS と Amazon SQS を用いた非同期化アーキテクチャの設計と実装
- Amazon OpenSearch Service を用いて顧客検索システムのパフォーマンスを改善
- 非同期アーキテクチャ、イベント駆動設計、マイクロサービス化

#### メルマガApp の開発

これまで AWS SES を使ってメール送信していたのを、AWS SESv2 を利用。SendBulkEmail を利用して、これまで 1 hour かかるような処理を 18 min 程度に短縮（約 1/3 の短縮）。
それによりショップオーナーが 1 日に送れるメルマガの上限を安全に緩和できた。
また ShopFront（購入者から見たショップの画面）からそのショップの顧客に登録できる、いわゆるメルマガ登録機能を作成。

#### アンケートApp の新規開発

Google Form / SurveyMonkey を調査、それぞれ参考にして技術仕様と全体構想/設計を策定し推進。
それぞれ技術領域が別れている Cart（購入カート）/ ShopFront（購入者から見たショップの画面）/ ShopAdmin（ショップオーナーが利用する管理画面）環境にて開発。

その後は CRM 関連機能を統括的に見つつメルマガ App やアンケート App など様々な BASE の Apps 開発を行う。

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

自社のサイトで、 `ドメイン変更` `サイト名変更` `全体のデザイン変更` などを含めたの大幅なリニューアルがありました。

私はこのプロジェクトに最初から関わり、主に開発メンバーとして参画しました。
上で挙げたリニューアルの観点とは直接的には関係しませんが、
そのそもそのサービスの前身が 2016 年ごろにかなりスピードを重視して開発されたもので当時スピーディに開発する選択肢として Rails を選択した経緯があり、今後手を加えていくのがかなりキツイ現状でした。

そのため、私含め開発メンバー4 人でリファクタリングを同時に進めていきました。

まず、携わっていたサービスはほとんどのデータのやりとりが API を介して行われていたため Virtus をいう gem を用いてオブジェクトの attribute を型定義し、API を介して取得されたオブジェクトと API を見える化しました。
アプリケーション規模も大きくなっていたので Rails way から離れリポジトリパターンを導入し、上記の Virtus を用いてエンティティをしっかり型定義し、リポジトリ層 Service 層と責務をしっかり明記することでアプリケーションの見通しを良くしました。

さらに、基盤をコンテナ化し ECS に乗せるうえでデプロイ手法も OpsWorks から CodePipeline に切り替えました。

また、webpack も導入し一部フロントも Vue.js を取り入れ新規の js ファイルはどんどん TypeScript で作成していけるようにしました。
Vue.js を取り入れたものの SEO の観点で SSR が求められるケースが多く、まだ jQuery で実装が余儀なくされることが多いのでフロントの Nuxt.js 移行が今後の課題に挙げられます。

また、サイトリニューアルに伴って影響範囲が全てのページにわたりました。
TDK, OGP, DataLayer, Json-LD に挙げられる meta タグ内のコンテンツも全て新規のものになりました。
それらのテストのために、以前から採用していた E2E テストも大幅に変更を加え、保守しました。その結果、サイトリニューアル時のテストはほとんど自動テストに任せれば良くなりリグレッションの早期発見や不安も取り除かれ、チームの開発効率が向上しました。

以上に挙げたほとんど全ての仕組みに私も携わり、中でも E2E テストの保守は私 1 人で行いました。

#### 地域情報に関連する記事更新の自動化
- MeCab
- Ruby 2.4
- AWS(EC2, CloudWatch, ElastiCache for Redis, VPC ピアリング、 AssumeRole)

自分が携わっているサイトの都道府県の LP（ランディングページ）で、その都道府県に関連した記事を表示するというものをやりました。

以前は手作業かつ、1 都 3 県のみ対応のサイトだったため記事は全て同じものを表示させていました。

サイトを全国化させていく中で、手作業は無理だしそれぞれの LP で記事を最適化させたいという要件が出ました。

そこで、私が提供元のサイトから記事を抽出し、MeCab を用いて記事を形態素解析し記事に対してそれぞれ都道府県への関連度を重み付けし関連記事として判定＆Redis に格納するバッチを作成し自動化させました。

「関連度」という抽象的なもののアプローチとしては形態素解析などの自然言語のアプローチ無くしては不可能だろうと考え、MeCab も触るのは初めてでしたが、ドキュメントや内部のコードを読み解きなんとかものにしてリリースできました。mecab の環境構築の際に標準の辞書データのインストールするのに 2GB 以上のメモリ容量が必要で使用が許された EC2 インスタンスが t2.small までだったらめ標準辞書だとインストールにギリギリ失敗していたので、分析に用いる辞書データを限定的に入れることで解消しました。

このプロジェクトは 2018 年 12 月〜2019 年 2 月で完全に私 1 人で開発しました。

同時に今回、バッチが動かす AWS アカウントと記事データを格納する DB を所有する AWS アカウントが異なることから、問題解決のための AWS の知見もかなり深まりました。

記事データを異なる AWS アカウントの S3 と Redis に格納する必要があり、S3 は assume role を活用し、Redis は VPC ピアリング接続して解決しました。

また、バッチの自動化のため CloudWatch Events、サービスオーナーへの通知に AWS SNS を活用しました。

このプロジェクトを完遂するまでは AWS にあまり詳しくなかったのですが、本プロジェクトを通してかなり AWS のノウハウがたまりましたので AWS Solution Associate 認定試験を後日受験し合格しました。

#### E2Eテストの保守/運用
- Selenium
- WebDriver
- Mocha.js

私が携わっているサイトの保守運用のための E2E テストを管理していました。

mocha.js というライブラリを利用し Selenium WebDriver を動かしています。

yaml で mocha.js の書式で書かれたものを展開してテストを実行するという手法を取っていますが、その仕組みは社内の独自のライブラリを使っているため、Selenium のバージョンが依存していてなかなか上げられていません。
そのため、まだ Selenium WebDriver のヘッドレス化かできておらず CI/CD に組み込めていないなどの課題感を感じていますが、サイトの大幅リニューアルなどもあり E2E テストを保守するので手一杯で改善に手が回っていませんでした。

保守とテストの管理を行う中で工夫していたことは、Selenium もとい E2E テストに明るくない開発者が如何にテストコードに手を入れやすくするかです。
サイトの開発者が DOM やセレクタを変えたら、その人が該当の E2E テストの箇所を改修できるようにドキュメントをまとめたり、コードを使いやすく抽象的にカプセル化し感覚で使えるよう修正していきました。

困難だったことは、やはり E2E テストを 1 人片手間で管理することでした。
E2E テストの保守と運用は知られているとおりなかなかに骨の折れるもので、社内のメインサービスの E2E テストでは専用のチームがあるくらいです。私が携わっているサイトはまだ発展途上のもので日々変更があるため保守の大変さに拍車をかけますが、チームで Selenium に知見があるのが少ないためほぼ 1 人で管理していました。
Selenium の知見が全くないメンバーだと簡単な E2E テストの追加や修正でも時間がかかってしまうということに課題感を感じ、Selenium の公式ドキュメントからよく使う WebElement 系の操作や WebDriver の待ち動作（until 系）のコードをメンバーに共有し、よくある E2E テストの追加や修正の例を示すことで他のメンバーによるテストコードの実装が比較的簡単になり負担を分散させることができました。

とはいえ、私も 2018 年の冬に E2E テストの社内ツールを触るまで Selenium の知見はなく、そこからサイトの開発の片手間にキャッチアップしていきました。今では自サイトの E2E テストの管理者として保守とテストの管理をしています。

### 株式会社NoSchool（2019/04〜2020/04）

#### WordPressで運用していたサイトのリプレイス（Laravel & Nuxt & AWS移行）

副業先の教育×テクノロジーの分野でプロダクトを展開しているところで、脱 WordPress をしていました。

Laravel を用いて 1 次のリプレイスは進めていたものの、フルで Laravel はフロントが辛いということもあり Laravel でどんどん API を作り Nuxt.js にフロントをリプレイスしていました。

そこで、私は管理画面系の Laravel & Nuxt.js のリプレイスと AWS の知見を生かしてデプロイや Route 53 や ALB 周りのインフラ設定について顧問的な立場も任されました。

Laravel でリポジトリパターンを採用しました。
admin 用の middleware を Laravel, Nuxt ともに作成し Redis を用いてセッション管理することで Laravel, Nuxt 両方からログインユーザの整合性の問題も解消しました。
Vue.js(Nuxt.js) を用いて画面部分の開発に着手する際、主に作成していったのは管理画面系でそれは内部の人が使うものなのでデザインは手早く組めるものを使用しいという理由から Vuetify を導入しました。
管理画面系は情報の網羅性が求められるため v-data-table はよく用いました。
v-data-table は多くの slot を用意しており slot の宝庫なので、v-data-table をどんどんカスタマイズしていく中で Vuetify の内部実装を見にいくことが多く、OSS として高度に抽象化されたコンポーネント設計を見ながら「何を Props に持つべきか」「どこを slot 化させるべきか」など学びも多くエキサイティングでした。
Vuetify の使用感はとてもよく、Vue のコンポーネント思想と UI フレームワークはとても相性が良いことを実感しました。

Vuetify を使い倒して知見も溜まったので、Vuetify_meetup というイベントにも参加して登壇しました。
こちらがその時の登壇資料です。

[https://speakerdeck.com/kimuchanman/fei-hurontoensiniakabao-su-tevuetifywoshi-utamenikiyatutisita6tufalsekoto](https://speakerdeck.com/kimuchanman/fei-hurontoensiniakabao-su-tevuetifywoshi-utamenikiyatutisita6tufalsekoto)

また、API 開発の際に、Laravel の JsonResource と TypeScript では aspida という HTTP クライアントラッパーの OSS を活用しました。
JsonResource を用いることで、Laravel 側の API レスポンスを最適化しなおかつ見える化しました。
aspida を用いることで Nuxt.js 側でも API が見える化され、なおかつ TypeScript の推論の恩恵を大きく得られました。知り合いが aspida の開発者なのも大きいのですが、aspida は個人的にも応援している OSS の 1 つで、以前紹介記事を Qiita に書かせていただきました。

[https://qiita.com/kimuchan/items/c60fbcb8e71baace0fc6](https://qiita.com/kimuchan/items/c60fbcb8e71baace0fc6)

### LIRIS（ライリス）株式会社（2019/12〜2021/02）

#### 契約ライフサイクルマネジメントサービスの開発

[https://clmlp.liris.co.jp/](https://clmlp.liris.co.jp/)

のフロントエンド領域を主に Vue.js で開発していました。
また、Cypress で E2E テストの導入などもやっていました。


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
