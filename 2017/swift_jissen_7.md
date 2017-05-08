# ✰実践Swift読書会 #7
## 12章 非同期処理

### 場所：Apparrayさん

- コマンドラインツールを作るのに
  - OperationQuesを利用　犬のアイコンの方
- GCD も Swift Core Library
- 優先順位を意識してない
 - 意識して利用したケースありますか？
    - 依存関係とは違う
    - デフォルトしか使ったことない人もいる
      - 画面を意識した更新をしたときに利用する
      - PromiseKitを使っているので意識しない
      - 複数のタスクを実行しているときに優先度を意識する
      - mixのiosトレーニング
      https://github.com/mixi-inc/iOSTraining/wiki/8.2-Grand-Central-Dispatch
      https://github.com/mixi-inc/iOSTraining
      https://github.com/mixi-inc/iOSTraining/tree/master/Swift
      - OSのコア数にもよる、
      - 共有の変数は排他制御が必要な場合、並列が遅くなる場合がある
- OperationQuesのなかで、mainキューとの使いわけ
 - p301はメインスレッドではない
  - GlobalQuesに情報を付加したイメージに近いのではないのか 
-
-
-
-
