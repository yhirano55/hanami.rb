## 成果物

- https://glacial-scrubland-37426.herokuapp.com/
- https://github.com/ShoheiMitani/hanami_payment

## 何を作ったか?

- 決済アプリ
  - 商品一覧作って、購入できるような感じにしたかった

## 工夫した or 苦労した or ハマったところ

- HerokuでMySql使おうとしたのが全ての間違いだった。。。

## Hanamiについて

### Pros

- erbに値を受け渡す方法がexposeで制限されている点
  - erbが変数地獄にならなくて可読性がたかそう
- appとlibに別れている点
  - 依存関係をapp -> libに統一すればappの肥大化が防げそう

### Cons

- erbにlink_to書こうとしたら、routes.rbをresources(getがだめ)にしないとダメだった
- routes.new_item_pathの`routes`が冗長な気がした

## Railsと比較した場合の感想

- コントローラークラスが多くなるのが気になる？（人によりそう）

## 実際に業務で利用したいと思ったか?

1. はい
2. アーキテクチャ設計でappとlibを分けるという視点はいいと思うから

## その他 感想（本イベントについてでも何でも）

- 環境構築らへんは先に行ってもらっておいた方が良いかも
