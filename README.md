# Slack sacloud

Slackを使用して、さくらのクラウド上のインスタンスをコントロールすることができます。

## Usage

### インスタンスの一覧を見る

```
/sacloud list
```

### 指定したインスタンスを起動する

```
/sacloud up <id>
```

### 指定したインスタンスを停止する

```
/sacloud halt <id>
```

### 指定したインスタンスを削除する

```
/sacloud destroy <id>
```

## セットアップ

`local.yml` というファイルをプロジェクトルートに以下のような内容で作成してください。
各種のAPIトークンはそこらへんからかき集めてください。

```
sacloud:
  SACLOUD_ACCESS_TOKEN: "xxxx"
  SACLOUD_ACCESS_TOKEN_SECRET: "xxxx"
slack:
  slack_client_id: "xxxx"
  slack_client_secret: "xxxx"
  slack_verification_token: "xxxx"
```

以下のコマンドを実行してください。

```
$ npm install
$ sls deploy
```

セットアップ手順をちゃんと書いてくれる人募集中です。
