
- day2 [iosdc2018.pdf - Speaker Deck](https://speakerdeck.com/shiz/iosdc2018)

- [iOSDC 2018 セッション資料まとめ - Qiita](https://qiita.com/winterwind26/items/210e5735d2ce832d0c36)
- [プロトコルを使って複数サービスを跨いだmusic playerを実装する - Speaker Deck](https://speakerdeck.com/kumabook/purotokoruwoshi-tutefu-shu-sabisuwokua-idamusic-playerwoshi-zhuang-suru)

## 重要
- [【完全版】AutoLayoutエラー診断所 ~発狂しないためのデバッグ手法~ - Speaker Deck](https://speakerdeck.com/akatsuki174/wan-quan-ban-autolayouterazhen-duan-suo-fa-kuang-sinaitamefalsetehatukushou-fa)
- [facebook/chisel: Chisel is a collection of LLDB commands to assist debugging iOS apps.](https://github.com/facebook/chisel)


## iOSマイクロインタラクション入門
- [iOSマイクロインタラクション入門 @koga_wiwi #iosdc #a - Togetter](https://togetter.com/li/1262760)
-

## ライブ配信アプリのアイテム再生をMetalで実装する事になった話
- [ライブ配信アプリのアイテム再生をMetalで実装する事になった話 - Speaker Deck](https://speakerdeck.com/noppefoxwolf/raibupei-xin-apurifalseaitemuzai-sheng-wometaldeshi-zhuang-surushi-ninatutahua)
- [ライブ配信アプリのアイテム再生をMetalで実装する事になった話 @noppefoxwolf #iosdc #b - Togetter](https://togetter.com/li/1262773)
- UIImageでアニメーション -> 途中でクラッシュ
- mp4でやっとるんか
- Metal

## デバイス・OSバージョンの依存が少なく、メンテナンスしやすいビューを作る
- なんでレイアウトが壊れる？
    - 特定の状態の時だけ起きる
    - 正しさの定義が難しい
- folioにおるんか
- 何が問題か
    - viewは状態が多い
    - ダイナミックに変化する
    - 実行せずに確認する
- アンチパターン
    - デバイスを判定する
    - 標準UIのサイズの判定をする
- 標準UIのサイズの判定をする
    - 変わらないと思っているものは意外と変わる
    - ケースを網羅するのは困難
- 通話中のUIどうなってる？
- safeAreaを使う
- AutoLayoutの制約をどうする？
- stackView便利
- pagingViewに対してもStackViewが便利
- UICollectionView vs StackView
- パフォーマンスはトレードオフ
- 実行せずに確認できる手段を増やす
- [folio-sec/Folio-UI-Collection: UI components and live documentation for Folio iOS app](https://github.com/folio-sec/Folio-UI-Collection)
- [iOSDC2018](https://www.icloud.com/keynote/04D-AD3CJxQh0U2IqjRmtxQBQ#iOSDC2018)


## iOSアプリの開発速度を170%に向上させたデバッグノウハウ
- [iOSアプリの開発速度を170%に向上させたデバッグノウハウ / Debugging knowhow that improved our development velocity to 170% - Speaker Deck](https://speakerdeck.com/orgachem/debugging-knowhow-that-improved-our-development-velocity-to-170-percent)
- ビルドしないで再実行できるんか
- stackframeをswiftまで戻すとlldbが効く
- セルフチェックどこまでする？
- コードの動作確認で自動化する
- XCTest
- [Presentations by Kuniwak - Speaker Deck](https://speakerdeck.com/orgachem)
- ↑あとで読む

## LLDBを最大限活用してみる。
- [miyasaka_iosdc_lldb_cfp.pdf - Speaker Deck](https://speakerdeck.com/miyasakakazutoshi/miyasaka-iosdc-lldb-cfp)
- 現在のコンテキストに沿った言語でないと実行エラー
- commandを短くする alias
- command regex を使うと、オプションの追加ができる
- コンテキストをmainにするとswiftで確認できる。lldb
- lldbにviewDebugerからドラッグ&ドロップできる。
- 今回のやつ使うと、自動で変数に入れてくれる
- パラメータ取れてたら、右クリックでメモリアドレスが取れる
- pythonで書ける
- python覚えてぇ

## weak vs unowned
- 参照のやつってああ使うのか

##
- 生活習慣大事
---
- [UICollectionView の Layout で悩んだら - クックパッド開発者ブログ](https://techlife.cookpad.com/entry/2017/06/29/190000)
- [継承を使わずにクラスにプロパティを設定する方法！ - Start Today Technologies TECH BLOG](https://tech.starttoday-tech.com/entry/ios_runtime_reference)
- [クラスを継承せず既存クラスにオブジェクトを保持する機能を追加する - Qiita](https://qiita.com/ryotapoi/items/3fe7218b93d8e2a61a2b)
- [[Xcode 8.2][新機能] アプリのシミュレーターへのインストールが簡単になりました！ ｜ Developers.IO](https://dev.classmethod.jp/smartphone/xcode-8-2-install-app-on-simulator/)
- [Playground駆動開発のすすめ / Playground driven development suggestion - Speaker Deck](https://speakerdeck.com/rockname/playground-driven-development-suggestion)
- [差分計算アルゴリズムを用いた高速なUITableView描画 - Speaker Deck](https://speakerdeck.com/fumitoito/chai-fen-ji-suan-arugorizumuwoyong-itagao-su-nauitableviewmiao-hua)
- [The iOS Timesさんのツイート: "DifferenceKit by @ra1028fe5 is a A “fast and flexible” diffing library with O(n) complexity for Swift collections, with UITableView and UICollectionView extensions https://t.co/asfqWYOZik… https://t.co/3P0JBVEO9L"](https://twitter.com/_theiostimes/status/1026555591278256128)
- [ra1028/DifferenceKit: 💻 A fast and flexible O(n) difference algorithm framework for Swift collection.](https://github.com/ra1028/DifferenceKit)
- [MicroViewController-en](https://www.icloud.com/keynote/0vgTYDXyHQTd0l1FKTiF1jT7g#MicroViewController-en)
- [レガシーなアプリケーションの 60fps化を目指す為にやっていること - Speaker Deck](https://speakerdeck.com/satoshin21/regasinaapurikesiyonfalse-60fpshua-womu-zhi-suwei-niyatuteirukoto)

- [iosdc2018.pdf - Speaker Deck](https://speakerdeck.com/shiz/iosdc2018)
