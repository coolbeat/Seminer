# ✰Swift実践入門読書勉強会
## 再利用可能かつ配布可能

### 発表者：佐藤剛士 さん
### 会社名/所属： MAMORIO株式会社


- privateを利用していて、extensionで少し拡張するケース
- 例
public class NameSpace {
   internal let name = "mamorio"
      public let number = 10
      //デフォルトがinternalだけど、可読性を踏まえると
      //意図的に明示しといた方が良い日もしれない
      let person = "sato"
 }
- 型全体がopen, public, 　
internalなら要素のデフォルトのアクセスレベルは
**internal**
//: * ->デフォルトでopne,publicにならないので注意！！

- privateにしているクラスはテストから見えない・・・
 - testabaleにすると呼べる
  - 結局テストできない!!

- privateを利用していて、extensitionで少し伸ばしておこう

- publicなインターフェースなクラスが呼ばれていて、
  - その中のプライベートな

- モジュールを作成するのは、自分で使う
  - OSSとしてgithubにしている
  　- どんなやつ？　＝＞　１行
    - shared extenstion

- アーキテクチャを使っている人
 - mvp,cleanarchtecture
 - mvvm
 - mvc

- フレームワークを作る目的
 -　ビルド時間を短縮する目的
  - ビルドがモジュール単位で、モジュールを含めるかの指定ができる
　- fireFoxの公式アプリ　   
    ビルド時間が早いという話がtry!swiftであった

- swift では Dynamic　フレームワークしかつくれない。

- ドキュメントコメント　option+command+スラッシュで一変に出てくる
- throws は、空文字返すのは申し訳ないので利用している

- クリーンアーキテクチャによる責務の分離にフレームワークを使う
https://speakerdeck.com/takasek/ok-li-xiang-falseakitekutiyahafen-katuta-de-dokokarashou-wotukenfalse
