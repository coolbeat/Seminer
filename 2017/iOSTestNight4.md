# iOS TestNight #4

## 発表タイトル：「AppiumからXuiTest」
### 発表者：根本さん
### 会社名/所属：メルカリ

- UI/E2Eテストがメインで作業している
- ios/Android　50%自動化を目標
- iosは、Appiumをやめて、XCuiTestに変えた
 - 理由１：・アクセシビリティの付与。アクセシビリティが振られているものが少なかった。付与しながらテストを書いていく事がAppiumには大変
 - 理由２：動作速度と安定性
 　　xPathを使うと動作が遅くなる
 - XCUIテストを試しに利用したら良かった
  - １つのレポジトリでAccessibility付与・UIテストが可能
  -
  - 実行速度Appiumより早かった
  - ページ遷移させるときにwaitさせることがある、waitもPageObjectパターンが利用できる
-　jenkins、社内MacからChatでキックできる
- リリース前のデグレッションテスト50%成功
-　取り組んだが、アプリはリリースされなかった
-　知っておくと便利
　- 並行実行（Bluepil,pxctest)
  - snapshot
- 違うチームで自動化の導入が検討することができた
- 定期的に勉強会をしている
- 自動化に興味を持ったQAエンジニアが出てきた

## 発表タイトル：「XCUITTestをする時のTips　〜あなたを助けるXXCUITTest〜」
### 発表者　@PooHSunny
### 会社名/所属:　リクルートジョブズ

- UIテストのアンケート
 - Appium 3,4人くらい
 - UIテストをしている人 10人未満
 - UIテストをしたい　ほぼ全員
- どこまでテストをすべきか
 - スコープ少ない方がいい
  - スモークテスト
   - 基本的な導線
      - a
   - 落ちると重大障害になる部分
      - 利用規約が潰れている
- UIを変更したら沢山のテストがこけてしまう。
　- UIを変更すると 10、２０箇所つぶれてしまうことがある
- ページオブジェクトパターン
 - テスト対象
  画面に張り付いたアクション、ボタン、テーブルを別のオブジェクトとする
   - 要約
    - publicメソッド＝＞ページが提供するサービス
    - UnitTest
    　- 下記のように分割すると変更が楽になる
     - Module //各ページ共通する部品
- このテスト何しているかわからない
　- 半年後なにしているかわからなくなることがある
  - テストの可読性を上げる
   - 利用メソッド名を日本語にする

- Given-When-Then意識してみる
　- 他にも考え方として　4 phase TestNight
  - 3A
    Arrange -act -Assert
- UIテストは自分たちを助けるテストとしよう


## 発表タイトル：「Pull Request時の画面差分取得自動化」
### 発表者　前田隼輔さん
### 会社名/所属:　DENA

- DENA SWET
 SWET　・・・　ソフトウェアエンジニアテスト
- Dangerでチェックができる
- fastlaneでsnapshotを利用してスクリーンショットをとる
- スクリーンショットの差分　imageMagicを利用する
 - compositとidentifyのコマンドを利用する
- キャプチャ画像をリポジトリで管理する
　- faslaneのlaneを追加する
- GitHub　Pull Request
　 画像のレビューがしやすい
- .xib/.storyBoard/.stringに変更があった場合
-　差分をみるときにきをつけること
  - ステータスバー
  　- 非表示
  - 自動スクロール
  　-　目的の要素が表示するまでwaitにする
-

-

## 発表タイトル：「UIテストの実行時間の短縮の方法」
### 発表者 平田さん
### 会社名/所属:　DeNa

- テストの実行の並列化
-　課題
　-　テストの実行時間
　　-　30,40,数時間となるケースが有る　
　-　解決方法
　-　テストのためにビルド
　　- build for testing
   - テストを実行
    -  
 -　実行時間を比較する対象一覧
 - FSSimulatorControler
    - facebook
- 実行時間
 - fastlane scan 392秒
 - bluePill　シミュレータ数 165.9秒

- さらに、テストクラス毎に経過時間のバラ付きがある
　- テストを最適化できる
  -　ポメラニング機能
  　ークラス単ににおける実行時間に基づきグルーピング

## 発表タイトル：「StubるMonkingjayを使ったHttpクライアントのテスト」
### 発表者　田中賢治さん
### 会社名/所属:クラス・メソッド

- 通常のユニットテストの流れ
- HttpクライアントのテストをするためにStubライブラリ

-oHHTPStubｓ
  - 上手い使い方が見つけられなかった
- Monkingjay
  - swift製
  　- Qitaに関係する記事があった
- stub:テスト対象のクラスの動作をサポート
- MOCK：メソッドが呼び出されていることを確認する
-

## 発表タイトル：「テストコードをアプリケーションコードと同じ階層に置きたい」
### 発表者 菊池さん　@Kikuchy
### 会社名/所属: 株式会社Diverse

- 関連あるものは同じところにおきたい
　- 実装とテストコードが離れている
-　同じグループを配置する
 storybardも、testファイル,
 Logerというツールを作成
  - テストファイルをアプリケーション側からテスト側に整理をしてくれるツール
  - swiftLintとは相性がわるい issuに上がっている
--
-

## 発表タイトル：「開発で学んだUnitTest５つのTips」
### 発表者 広瀬緑
### 会社名/所属: リクルートジョブス

- 本日お話すること
-　初心者がUnitTestを書いてみて学んだこと
-　Quickを利用している
　-　GibenWhenThenを意識する
　- expectの中身に処理を書かない
　-　1つのiｔに対して１つのexpectにする
  -　テスト出来る設計にする
- プロダクションコードに手が入っているよ。
- Mockを利用して通信でのレスポンスをテストする
-
-

## 発表タイトル：「実践 bulepill」
### 発表者: kamiyaさん
### 会社名/所属:ユビレジ

- 前回のiosテストナイトで紹介されたBluePilを試した
- 試したけど動かない
　-　case sensitive File Systemsで大文字、小文字が判断できない。
 - テストケースが多いとハング、
  - 1000テストと動かない
   NSTestとNSTask
-　fastlan scan
 - - build xxがある
- fastlan scan 495秒
- bluepill　
-　waitが挟まるテストの場合 効果がある
 - メモリはあれば、あるほどよい
 - Travice Ciで効果がでた
  -
- BluepillのデバッグはObjective-Cで書かれている

## 発表タイトル：「テストを書かない言い訳をした結果」
### 発表者 takasekさん
-  テスト書きたくない理由
 - テストファイルへの距離が遠い
 - テスト負債になりやすい
- テストファイルへの距離が遠いの解決
 - ファイルをならべておく
   - レガシーコードにも書かれている
　-　Xcode source Editeor Extensionもつかいもんにならんらい
-　appliescript + XcdeBehabior を利用して
　XcodeBehabiorのカスタムでショート・カットキー


## 資料
http://dev.classmethod.jp/smartphone/iphone/event-report-ios-test-night-4/?utm_source=dlvr.it&utm_medium=twitter

https://speakerdeck.com/takasek/tesutowoshu-kanaiyan-iyi-wositajie-guo-wwwwwww

https://www.slideshare.net/mobile/HiroshiKikuchi/ss-76203123

https://www.slideshare.net/mobile/kenjitanaka58/stub-mockingjayhttp

GUI的に遠いという話が割と出たりするけど、⌘ + Shift + oでジャンプすればええやんと思ってしまう派
#ios_test_night

https://speakerdeck.com/poohsunny/xcuitestsurushi-falsetips-anatawozhu-keruxcuitesthe

https://www.slideshare.net/mobile/ShunsukeMaeda/pull-request-76210799

https://www.slideshare.net/mobile/tarappo/ui-76205186
