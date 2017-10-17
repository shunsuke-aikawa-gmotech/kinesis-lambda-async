# AC2 プッシュ開封アクション
## システム概要
AppCapsuleの大規模クライアント用システム（通称AC2）のプッシュ通知開封時アクションを行う

kinesis stream -> lamdaで動作させることを前提としている


### 使用ライブラリ
lambda.json参照
- SQLAlchemy
- MySQL-python
- lambda-uploader

### ディレクトリ構造
- app
 - controllers　コントローラー
 - models　モデル
 - modules　共通機能
- conf
 - app.json　アプリ情報　アプリ名、ステージを決定する。
 - policy.json　デプロイ時に参照する。
 - settings　環境ごとの設定ファイル settings.pyを読み込む。対象ファイルが存在しない場合はsettings.pyを読み込む。
- lambda.json　デプロイ設定ファイル
- libmysqlclient.so.18　ここに置かないとlambdaが参照しない
- deploy.sh　デプロイスクリプト

