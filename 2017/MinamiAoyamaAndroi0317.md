# inami Aoyama Night#2

## STFとAppiumを使ってUIテスト工数を半分にした話
### 発表者：萱島 克英さん

### 会社名/所属：株式会社ナビタイムジャパン
#### 発表内容

- STF
  - HomeBrewでインストール出来る
- AppiumとSTF
  - テストコードはRuby
  - 日本語入力が不明・・端末によりIMEが異なる
    - Google　日本語入力をインストールしてデフォルトにする
  - AppinumサーバーにChromeDriverのバージョンを最新にする
    - Debuggint?? True
- Docker for Mac
      - コンテナ内からUSBドライバを接続できない　＝＞Vagrant利用
- リグレッションテスト　効果
  -　20%自動化
  - リグレッションテストの工数が半分
  - 課題
    ― プログラムスキルが必要 習得工数がかかる
    - Appiumからintent連携 連携でChromeを開き、期待した画面が表示することがはできない
  - 全ての操作を自動化しない
  - 検証サーバーを安定にしておく、落ちたらテスト不可

 - opnestf/stf
 stf-appium-example
  -STFに接続された端末にAppium経由でテスト実行する

 -　質疑
  - Q:ABテスト等で頻繁に変わる画面にテストを行うか
  　- A：テストをしない


## VASILYでのアプリ開発における自動化の取り組み

### 発表者：株式会社VASILY

### 会社名/所属：堀江 亮介さん
#### 発表内容

- 会社紹介
  - iQONというアプリを開発
    - 会員録 250万
    - SNAP
     - Deep Leraningを利用して似たようなアイテム
     　を購入させるサービス
- 開発体制
  -アプリ開発部
    - ios 3人、Android 2人（インターン１院）
  - デザイン部
  - 開発部
    -バックエンド　
      - API クローラー　インフラ
- 自動化
  - 目的
    - 楽をするため
    - 自動化する自体楽しい
    - 業務効率、生産性を向上するため
    -求められる品質・スピードを実現するため
  - 成果
    - 品質
      - 低クラッシュ率
      - バグが少ない
   - Ci/CDの環境
      - ios TravelCiでビルドのみ実行
      - Android jenkinsからサークルCI
      　４GBのサークルCIの問題ありー＞Werkerに変更
      -　社内へはFabricのベータで展開
      - androidはアルファ版から製品版にリリースにする
   - MVVM　もしくは MVP
     - プレゼンテーション層はしない　コストが高い
        - レイアウトが頻繁に変わるため
        - Firebase Test Lab
          - tec labのWebページに記事がある
    - UIの設計と実装
      -　やり取りが多く発生すると効率が悪い
        - できるだけ減らしたい

      - sketch,zplinを活用
      -  zeplinで仕様確認
      - apiaryを利用している、
    - QA
       - Quit:Teamを利用している
       - 手順を自動化した
    - 開発以外の業務改善
        - 定例ミーティング資料の自動生成
         - slackからBot経由で作成
         - Quita APIを活用
         - 手動で作成する時間を削減
        -　社内チャットでBot勉強会を開催
       　 - Botを作れる人を社内でふやしている

      - 質疑
      　- Q:ミーティングの資料を自動化とはどんな感じなのか？
      　　  - A：[ミーティング資料自動化のリンク](http://tech.vasily.jp/entry/android_qa_automation)
        - Q:Zepplinへ書き出すのはデザイナーさん？
          - A:出力するのは デザイナーさん
       - Q:今後自動化をかんがえていること？
          - A:　APKを自動で取得したい
       - QAで気になったこと
          - A:skechからinvisionに吐き出すとき
          　 - ファイルサイズが大きい

## Pairsのデザインガイドラインを作って開発を効率化した話

### 発表者：株式会社エウレカ

### 会社名/所属：二川 隆浩さん @futabooo
#### 発表内容

- pairs
  - 技術
  -　javaとkotolin　半々
  - Android ,ios, Web ,mobileブラウザの４つのデバイス

-　４つのデバイスへの変更
  -　デザイナさんの負担が大きい
    - デザインカンプがある
    　 - レイアウト・・・・
  - デザイナー　１人対して、エンジニア、Androd,iosのデザインをみていた
    - 対策
     -
   - デザインガイドライン？
   　  - googleのマテリアルデザイン？
   　  　―　googleのマテリアルデザイン資料は整っているが
          -　googleのマテリアルデザインまで詳細にやっている時間がない
            - デザインガイドラインを作る
              - ３ヶ月　(他のタスクと並行
                )
              - メンバー　web２名、Android, ios ,デザイナーのメンバーで作り上げる
              - 参考：[エンジニアリングにおけるuiコンポーネント指向の考え方と協働について](https://m.axross.io/エンジニアリングにおけるuiコンポーネント指向の考え方と協働について-2c3dbca01ab9#.kwel1248h)
              - ダイアログ
                - タイトルとメッセージだけもらってエンジニアが実装する
              - 訴求（この期間だけ◯◯しますよキャンペーン）
                - 画像だけもらうだけ

    - デザインガイドラインを作成しことで
      - ガイドラインにない部分だけコミュニケーションが発生する
        -　デバイス毎のずれが発生しなくなった
        - デザイン適応のためにコードのリファクタリングをしたので、コードもキレイになる
        - 今後の課題
          - sketchファイルが重い
        - 既存の洗い出しが大変
          - 色
          - ボタン
          - モーダル

    - 質疑
      - Q: デザインガイドラインのないものはどうするのか？
      　- A: エンジニアがデザイナーと話して、新たに作成しているが、他のデバイスもコミュニケーションの見える化も大切、残して置くこと

      - Q: Abstract  App sketchがある

      - Q: ガイドラインはデザイナー、エンジニアどちらが手動か？
        　- A:　両方、エンジニアもSketchが扱える

    資料！！！


# HOME’SアプリのFragmentとデザインの関係

### 発表者：株式会社ネクスト

### 会社名/所属：寒川 明好　さん
#### 発表内容

- Home'sアプリの歴史
  - リリース2014年9月にリリース
  -　これまで６１回リリースしている
    - リリース当初は、Activityと複数のFragmentの構成
    - Fragmentが保有するViewに対して複数のFragmentをAttachしていた
      - しかしsupport librayのバグで、add順で表示されない
        - マテリデザインへのシフトを行う
          - scroll したら常に　表示する　とか スクロールするとToolBarに納まる
          - ベースとなるAcitivyから移植
            -現状は、機能ごとにActivity,
            - 1画面は1Fragment
              - Acitivty
                - main
                 - 商品を検索するルート
                - scheme
                - Detail
                 - 商品詳細
                - setting
          - 画面遷移をActivityが役割をしていて
          　 - FragmentにインターフェースをもちActivityから遷移
          -　Fragmentが大量にスタックされている
            - 画面回転時や アクティビティがはきされる
             - OS7 からTransitionTooLargeExceptionがハッセい
              再生時にスタックしているFragmentはしる
              - 対策としてUIを持たないFragmentをもちsetRetainInstance
              そもそもbackStackにいれるな =>
              google ドキュメントに記載ある

- 複数人で開発しているので　Fragmentの抽象クラスにViewが紛れる
 - DataBindingの導入が大変。

- 1画面1Fragmentの構成
  - ボタン同時押しなど画面遷移が複数はしってしまう.
  - splitmotionebents(false)で抑制
- FragmentのButtonをタップしたら DialogFramentを表示
  - childFragmentマネージャーで管理
  
  - coordinatorLayoutを利用することで
    scrollbarに動的なレイアウトを実装
  - Fragmentの管理は大変
    - setRetainInstance(True)であkんリ


- Home'sにおけるActivityとFragment
