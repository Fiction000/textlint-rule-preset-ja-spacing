# textlint-rule-spacing [![Build Status](https://travis-ci.org/textlint-ja/textlint-rule-spacing.svg?branch=master)](https://travis-ci.org/textlint-ja/textlint-rule-spacing)

[textlint](https://textlint.github.io/)のスペース関連のmonorepoです。

日本語周りにおけるスペースの有無を決定するtextlintルールプリセットを提供します。
それぞれのルールは個別のモジュールであるため、必要なルールのみをインストールすることも可能です。

## ルール一覧

### [textlint-rule-ja-no-space-between-half-and-full-width](./packages/textlint-rule-ja-no-space-between-half-and-full-width)

半角文字と全角文字の間にスペースを入れないようにするルール

### [textlint-rule-ja-space-around-code](./packages/textlint-rule-ja-space-around-code)

インラインコードの周りにスペースを入れるかを決めるルール

### [textlint-rule-ja-no-space-between-full-width](./packages/textlint-rule-ja-no-space-between-full-width)

全角文字同士の間のスペースについてのtextlintルール。
全角文字どうしの間にスペースを入れません。

### [textlint-rule-ja-nakaguro-or-halfwidth-space-between-katakana](packages/textlint-rule-ja-nakaguro-or-halfwidth-space-between-katakana)

カタカナ語間の区切り文字についてのtextlintルール。
カタカナ語間は中黒または半角スペースを用いてカタカナ語を区切ります。

### [textlint-rule-ja-no-space-around-parentheses](packages/textlint-rule-ja-no-space-around-parentheses)

かっこの外側、内側ともにスペースを入れないようにするルール

### [textlint-rule-ja-space-after-exclamation](packages/textlint-rule-ja-space-after-exclamation)

文末に感嘆符を使用し、後に別の文が続く場合は、直後に全角スペースを挿入します。
文中に感嘆符を使用する場合はスペースを挿入しません

### [textlint-rule-ja-space-after-question](packages/textlint-rule-ja-space-after-question)

文末に疑問符を使用し、後に別の文が続く場合は、直後に全角スペースを挿入します。
文中に疑問符を使用する場合はスペースを挿入しません。

## 開発フロー

1. [packages](./packages)に作成ルール名でディレクトリを作成
2. 作成したディレクトリに通常のnpmモジュール作成と同一のフローで作成

その後、`packages`全体について操作したい場合は`lerna`を使います。

- [Lerna · A tool for managing JavaScript projects with multiple packages.](https://lernajs.io/ "Lerna · A tool for managing JavaScript projects with multiple packages.")

全てのpackagesの`npm install`:

    npm run bootstrap


## Tests

以下のコマンドで全てのルールのテストを実行できます。

    npm i -d && npm test

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

MIT