# iOSDC2018 day0
- [Playground駆動開発のすすめ / Playground driven development suggestion - Speaker Deck](https://speakerdeck.com/rockname/playground-driven-development-suggestion)


# iOSDC2018 day1

## ~~ †††† 漆黒の魔法 Objecitve-C Runtime API †††† ~~ a

### Method Swizzling
すでに実装されているメソッドを入れ替える

呼ぶメソッドそのものを変えることができる
 ex> viewDidLoadでも可能

 ```
method_exchahgeImplementations(originalMethod, exchangeMethod)
 ```

ライブラリ: `Segue additon`

### Enumeration Mutation Handler

for eachの途中で処理を変更できるよ

objc_setEnumerationMutationHandlerでsetupしないとerrorを返すよ

どこで使うかわからん

## MicroViewControllerで無限にスケールするiOS開発 a

- メルカリのcellって全部ViewControllerなのか
- ViewControllerごとに人を分ける
    - コンフリクトが起きにくい
    - 設計がシンプルになる
- ios1つのアプリに20人エンジニアぶち込んでる
- レイアウトの実装が簡単になる
- 表示速度が3倍になった -> PV数がのびた
- なんでViewじゃないのか
    - 画面遷移、ライフサイクルがfatになる
    - ViewControllerにすると親が見えなくなる
- XibはAutoLayoutをチェックできる唯一のツール
- __VCでやることでロジックを保持した状態で分けることができる__
- 3つのプロトコルに縛ることで、結合がしやすい
- かなり強い型プログラミングができる
- containerViewExtensionが入出力を管理する
- リクエストの対してレスポンスを返す物を全部overroadしてる
- microProjectにすることで、コンフリクトが減る
    - 循環参照を解決してる
- xcodeTemplateを作って効率化
- [mercari/Mew: The framework that support making MicroViewController.](https://github.com/mercari/Mew)
- いいところ
    - view -> 500ms以内
    - 開発速度　-> x2
- 画面遷移はrootVCは使ってない。VCがそれぞれ保持している
- 親は親が知るべきイベントのみを知る
- 責任をどんどん子に移譲していく
- ABテストの際に、VCに依存できるし、エラーを直して、それを捨てるだけ
- 一人でやってても、機能を分けれるから、機能変更がしやすい
- viewModelもそれぞれのVCに移譲してる
- tableViewCellにVCを入れている
- 個別のコンポーネントがイベントを発火できる
- グルグルのインディケーターを出すのが必須

## 安定したチャットを実現するためのアプリとAPI設計 a

- coredata vs realm realmの方がパフォーマンスチューニングがしやすい
- 送信ボタンを押した後にアプリを閉じても送信される
- offsetPagination(問題が起きたり) -> TimelinePagination(slackとか)
- 送信開始時点でメッセージは永続化しておく
- UICollectionViewがいい理由
    - UICollectionViewLayoutが使える
    - 柔軟なレイアウトができる
- ScrollToBottomが必須。ハマることもある
- スクロールの位置を維持したまま、アイテムを追加する。
    - アイテム追加前にcontentOffsetを保持
- keepingContentOffsetCollectionViewLayout
    - [KeepingContentOffsetCollectionViewLayout.swift](https://gist.github.com/muukii/29249c295a0f2c4fecde61d99abc94f5)
- 簡単な解決策：tableViewを逆さにする。
    - ScrollToTopになるから楽
    - アイテムが少ないときの表示をするのが大変
- growing textViewの実装が必須
    - どこまで伸びるのが有効にするかの設定次第で、難易度が上がる

## コンパイラから紐解くSwift method dispatch b

- [コンパイラから紐解くSwift method dispatch - Speaker Deck](https://speakerdeck.com/kateinoigakukun/konpairakaraniu-jie-kuswift-method-dispatch-1)

## 宣言的UICollectionView a

- [Declarative UICollectionView - Speaker Deck](https://speakerdeck.com/ishkawa/declarative-uicollectionview)


## Swiftコードから状態遷移図を自動で生成し、継続的にメンテナンスしやすくする a
- ステートマシン
- AST
- flow-graph
- swift Package Manager
