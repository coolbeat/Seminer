# Android Testing Bootcamp #6

## タイトル：　
### 発表者：　Tatuya Shimada　さん
### 会社名/所属：リクルート住まいカンパニー

-- Tange
- AR体験を実現してくれる端末
  - MotionTracking
  - DepthPerception
  - AreaLeraning
- 精度：５センチ前後
- LTドリブン改善　LT発表してから２週間で改善した
- 問題点整理　
　- コードの結合が密結合
- 開発ツールを再選定
- 社内はconfuluence
- 設計方針　mvp
  資料としてmvpを選定
  UniRxがあるのでmvp

- unityに単体テスト機能ガある TestRunner

- unite2017Tokyo unity.2でTangoのnativeサポートされた

- 資料
 https://www.slideshare.net/shimadatatsuya/ar-unity-project

- - -

## タイトル：　high cost performance CI
### 発表者： Yuta Tetuka
### 会社名/所属： ジャストシステム

- CI
 - Github Enterprise + Jenkins
 - Github Enterprise + CI as a service

- Cost Caluculation
Github Enterprise
 - 2.500/ 10-
-Ci as a service
 古いビルドシステム

- GitLab
 gitlabは貧者のGitHub

- 2013年からsvnからgit
 - 入れるなら選択肢とコストを計算して
 -
- gitlab
　- 使い勝手が良い
 - 月１回アップデート
  - 看板はgithubよりいち早くリリース
  - Burndown Chart

- gitlab CI
  -GitLabとは別に、Runnerサーバーを用意が必要
  - windows linux mac
  Excutor
   - Docker
   - shell ランナーサーバー上で動かす
   - virtural box
   - ssh
- コスト　Gitlab,GitLabRunner 0円
- Build Docker image
 - 新しいプロジェクトの下に DockerFile,android-sdk-lincence
   .gitLab-ci.yml
  ※ ビルドが成功するとDocker イメージが出来る
- CI FeedBack
 - ビルドが通らないとマージリクエストを受け付けない機能がある
- GitLab.com
  - gitlab jp Community
    - slack
       https://gitlab-jp
- 質問
  - Q:instarmentalテストはどのくらいの数ができるのか？
  　- A:試していない・・・動作速度は不明
  - Q:GitLabはGitHubEnterPriseに比べてどこが優れているのか
  　- A:正確な機能比較の言えないが、コスト、多種のマイクロサービスが出ているので組み合わせられる
  - Q:
- - 資料
https://docs.google.com/presentation/d/1IS7qFrzJxwPozr7I5s0ot88HhhaSn_wYvk4ae7i71Is/edit#slide=id.g35f391192_00
-  

--
## タイトル：弊社のアプリ開発のCI環境　
### 発表者：
### 会社名/所属：LeadingMark

- アプリ紹介
- レクミー、レクミーキャリア
　- 新卒サービス、転職サービス
- アプリ開発のCI環境について
- IO,Androidエンジニアは発表者だけ

-　環境
　- github ,CIはjenkins(mac mini)
　- slack、配信用：Fablic
- GitFlowを採用
- gitHubFlowは高速でリリースするイメージ、テストコードも完全に
　入っていないので、GitFlowを採用
- jenkinsの採用
 - iosアプリのビルドも考慮
  - circleCiだと最小プランで月39ドル
 - 環境（SEKやAVD)をこちら側でコントロールできるので
- jenkinsを使うときの注意点
-　カバレッジを１００パーセントの実現は、現実的に難しい。
　何を入れたら何が返ってくることかを保証すること
- 人力テストでしんどい点、変更点は無いけど影響しないことの確認が
　しんどい。
 - appniumいいよね。
  - MagicPodと言うサービスがある、appiumのテストが簡単に作れる
   - 人のテストで雑になる。テスト漏れがある可能性がある
   　- developの更新＋毎朝X時に走らせてる
   - MonkeyRunner（Googleが適応）
- CI の発火
　プルリクをしたタイミング
- MagicPod
 - 画面を作り直したときにはキャプチャの取り直し
  - やりにくい画面もある
  　- 解決予定のようだ
   - androidだと微妙にタッチ領域がずれる

- 資料
https://speakerdeck.com/yamacraft/bi-she-falseapurikai-fa-cihuan-jing
-

--
## タイトル：　Using Kotolin for tests
### 発表者：　愛澤 萌 @lvla0805
### 会社名/所属： サイバーエージェント

- Kotolinの紹介
- getFullNameのテストをしてみる
- Kotolinだとis,whenは予約後なのでTestではシングルクォーテーションを付ける
- Knit Kotolin向けのJunit
- Kmokito Kotolin向けのmokito


- 質問
　- Roboletricとの共存できているのか？
　　- 共存ができる
 -

- 資料
https://speakerdeck.com/lvla/using-kotlin-for-tests#
-
-  

--
## タイトル：　Annotaitionを用いた現時刻のテスト
### 発表者： 外山さん
### 会社名/所属：ヤフー株式会社

- mokitoでspyメソッドで振る舞いを変える
- yukimatumura/Now
　- gitHubに資料がある
   - 上記を Kotolinを使うとわかりやすくなる
  コンストラクトで宣言でき、int型でもたせることができる
- 資料
https://speakerdeck.com/egugue/annotationwoli-yong-sitaxian-zai-shi-ke-falsetesuto

--
## タイトル：　ノハナノハナシ
### 発表者：　せとさん
### 会社名/所属：株式会社ノハナ

- リアルの話
 - テストをkotolinで書いている
- CIはTravis（有料）
　　サーバー側が利用しているので
- プルリクなげるとTravisCIが
 Travis Cron JobでinsstarumentTestを行うようにした

- Roboletric Cusotm Shadow
 - statiメソッドのmockできる

- 資料
-
https://speakerdeck.com/seto_hi/falsehana-false-tesuto-false-hanasi-1

http://blog.nohana.co.jp/article/droidkaigi2017

--
## タイトル：　mvpアンチパターン
### 発表者：きりみん　さん
### 会社名/所属：　フリーランス

- ViewとPresenterの責務わけ
　- ActivityやFragmentを直接参照すると責務訳が崩壊する

- issueをたてて設計

・ Viw -> presenter -> userCase -> Repository
- Robotoriticを使いJunitTestとして実行

- 既存画面を順次リファクタリングする

- presenterのテストだけだるとだけだると画面全体がテスト出来る
- prdrnterがFatになるとロジックの切り出しをすることを検討

- presenterを再利用する実装を検討している
- view - presenter - usecaseは１画面１セットしている
- 再利用したい場合は、モデルに切り出している
- 資料
https://speakerdeck.com/kirimin/refactoring-mvp-anti-pattern


--
## タイトル：　DevieFarmを諦めた話 あるいはUIテストについて再考する話
### 発表者： mochicoさん
### 会社名/所属： Techbooster

- minneアプリの話
- github flow
- mvp
- github Enterprise
- AWS Device Farm
　- すべてのPUshで動くようにしていた
　　- １端末専有契約にした
- 　　セットアップから実行まで10-40分かかる
　- 謎のエラーでめっちゃ落ちる
　　　 - 不安定
- 実機で動くことを確認したい
 Firebase Test Labに無料枠！！！
安定して実行できる

雑誌
Androidアカデミア

- 資料
https://speakerdeck.com/mochico/how-use-android-testing-service
-
--
## タイトル：　軽量なDokerイメージで
### 発表者：堀江さん
### 会社名/所属：VASILY

- Alpha linux


-資料
https://speakerdeck.com/horie1024/qing-liang-nadockerimezide-cifalsebirudoshi-jian-woduan-kusitemiru
-
