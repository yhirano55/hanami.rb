## 成果物

- https://localhost9292.herokuapp.com/
- https://github.com/yhirano55/hanami-example-app

## 工夫 or 苦労した点

- チュートリアルをなぞっただけではある。
- hanami newの時点で、template=slim test=rspecのオプションをつけたので、そのまま実行できなかった。
- herokuデプロイするときの謎の環境変数の正体は以下っぽい。
- Railsと、いろいろ違うので苦労。

```ruby
# config/environment.rb:42
  environment :production do
    logger level: :debug, formatter: :json, filter: []

    mailer do
      delivery :smtp, address: ENV.fetch('SMTP_HOST'), port: ENV.fetch('SMTP_PORT')
    end
  end
```

## Hanamiについて

触りレベルの触れ方なので浅いのですが。

### Pros

- バリデーションがparamsで行うのが良い。
- RepositoryとEntityに分かれているのが良い。
- Sequel、慣れたらRailsのmigrateより分かりやすいかもしれない。

### Cons

- Entityに未定義の属性を初期化時に渡しても例外が発生しないので間違いに気付かなかった。OpenStructみたいな雰囲気なのか?
- リポジトリでも初期化する必要があるのだが、newせずにクラスメソッドで実行できるといいのかな。

## Railsと比較した場合の感想

- ファイル間の往来が多い。
- Railsの場合、db制約をそのままモデルに書くことがままあるが、そのあたりのバリデーションがコントローラに紐づいていて良いと思った。

## 実際に業務で利用したいと思ったか?

1. はい
2. 理由: 言語が変わっても応用が効きそうな構成なのでよさそう（それを言ったら、Sinatraやrodaでもいいんだけど）

## その他 感想

