# POTATOTIPS 20170317

##

### 発表者： thiasa　さん

### 会社名/所属：楽天株式会社
#### 発表内容

- ラクパというアプリをリリースした
  - アーキテクチャ
    -  clean airchtecher
    - application Coordinator
- Application Coordinatorとは？
  = 画面遷移をコーディネートするもの
  - viperのwireframeの似ている
  - 画面遷移をコードにしたもの

- 資料
https://speakerdeck.com/takahia1988/application-coordinatorwoli-yong-sitahua-mian-qian-yi

## Practical Implementation of Up Navigation

### 発表者： こばけい　さん @Kobakei

### 会社名/所属：

#### 発表内容

- Nviutil.xxといううまくいかない
  - 再生性される
- Qiitaに記載がある。
　写真
- DeepLinkでupボタンを押下した場合
   - googleの検索画面に戻るのが正？
    - 登壇者は、他のアプリをみて、同じアプリに遷移していた

- 資料
https://speakerdeck.com/kobakei/practical-implementation-of-up-navigation

## 任意のテキストをパワポみたいにおしゃれに動かしたい

### 発表者：かずひろしくしく　さん Yahoo!Japan

### 会社名/所属：Kazuhiro Hayashi
#### 発表内容

- 文字をパワポみたいにしたい
  - LTMOrphongLabel
    - CADisplayLinkをつかってフレームごとに各文字を操作している
  - もっとio的に利用したい！
    - CoreTextとCoreAnimationを組み合わせてみてみる！
    　 - githubにサンプルある
       - CALayerに好きなアニメーションを適応される
       - 文字単位なんで、パフォーマンスがよくないが、LTMOrphongLabelよりは、良い

 - 資料
 https://speakerdeck.com/kazuhiro4949/ren-yi-falsetekisutowopawapomitainiosiyarenidong-kasitai-potatotips-number-38

## Let’s make Photo Frame with Android Things

### 発表者：ニイノミ　さん サイバーエージェントさん

### 会社名/所属：
#### 発表内容

- Android things はラズベリーパイで動かせる環境
  - 作品紹介
  - セットアップ方法
  - 開発 ピンタレストのAPIを利用している
  - ラズベリーパイからピンタレストのAPIで画像を取得したいが・・・
   -  Firebase のリアルタイムデータベースを利用する
    - Android -> firebase -> ラズベリーパイで取得

 - Android things は　プレビューバージョン
 - Android thingsのアニメーションが遅い

 - 資料
 https://speakerdeck.com/r21nomi/lets-make-photo-frame-with-android-things


## PropertyObserverとinoutでやらかした話
### 発表者：駒場さん @r_plus
### 会社名/所属：Hand Lab inc
#### 発表内容

- RXで xxを外した話
- objectMappable

## Coordinatorパターンの実践
### 発表者：かとう　さん

### 会社名/所属：
#### 発表内容

- coordinatorパターン
  - 画面遷移のロジックをVCから切り離す
- コンテナビュー

- 資料
https://speakerdeck.com/yoching/coordinatorpatanfalseshi-jian

## ConstraintLayout再入門

### 発表者：androhi　さん takahiro

### 会社名/所属： Finc inc.(有楽町にある会社)
#### 発表内容

- ConstraintLayoutってなんだっけ？
  - RelativeLayoutのすごいやつ
  - 相対位置が配置可能　柔軟な指定
  - xmlで編集しなくても、GUIから変更できる
  - Viewに制約をつけて動かす
  　　公式のサンプルがある

- Android studio2.3
  -テンプレートが
  全てがConstraintLayoutになった
  - アスペクト比
  - グループ操作ができるようになった

- 資料
https://speakerdeck.com/androhi/constraintlayoutzai-ru-men

## いまさらですがRxSwiftつかってみました

### 発表者：よねあっぷ さん

### 会社名/所属：　スタートアップ -> フリーランス
#### 発表内容

- アプリ「Tastime」をリリース
- push通知トークンの共有
  -　RxSwiftをつかってみよう

## MediaSessionの話

### 発表者：ピーサイド さん

### 会社名/所属：
#### 発表内容

- MediaSessionとは
  - 他の器機と動機をとる
  - サポートライブラリ MediaSessionCompatを利用する
  - MediaControllerくらすからの操作をCallBackで受ける
    - service等をintent受ける〜みたいな実装をかかなくてよくなる
  - Googleのサンプルコードがある

  - MediaSession
   youtubeアプリは、MediaSessionを利用して、AndroidWearと連携している

## えらーと警告でコードをデザインする

### 発表者：ezura　　さん

### 会社名/所属：
#### 発表内容

- エラー警告でこーどをデザインする
  - 資料
  https://speakerdeck.com/ezura/eratojing-gao-de-kodowodezainsuru-chi-tohuang-falselun-wu-qu
  - unsefeBitCast


## １人開発体制からチーム開発体制移行時にやることやったこと+α(仮)

### 発表者：からーぼっくす　　さん

### 会社名/所属：
#### 発表内容

- idobata　アプリ　リリース
  - 開発者向けのコミュニケーションアプリ
  - 1人=> 2人になった
    - swiftLintを導入　一旦全てFalseにして導入
  
