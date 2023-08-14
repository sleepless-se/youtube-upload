# YouTube Video Uploader

このプログラムは、指定された動画ファイルをYouTubeにアップロードするためのPythonスクリプトです。GoogleのYouTube Data API v3とOAuth2認証を使用して動画のアップロードを行います。

## 機能

- 動画ファイルのアップロード
- 任意のタイトル、説明、カテゴリ、キーワードの設定
- プライバシー設定（公開、非公開、限定公開）
- エラーが発生した場合のリトライ機能（最大10回）

## セットアップ

```sh
pip3 install -r requirements.txt
```

## 設定

- `client_secrets.json`: OAuth 2.0情報が含まれるファイル。Google API Consoleから取得できます。
- YouTube Data APIをプロジェクトで有効にしてください。

## 使い方

コマンドラインから以下のように使用できます：

```
python main.py --file=動画ファイルのパス --title="タイトル" --description="説明" --category=カテゴリID --keywords="キーワード1,キーワード2" --privacyStatus=プライバシー設定
```

各パラメーターの説明：

- `--file`: アップロードする動画ファイルのパス（必須）
- `--title`: 動画のタイトル（オプション）
- `--description`: 動画の説明（オプション）
- `--category`: 動画のカテゴリID（オプション）
- `--keywords`: 動画のキーワード、カンマ区切り（オプション）
- `--privacyStatus`: 動画のプライバシー設定。"public"、"private"、"unlisted"から選択（オプション）

例：

```sh
python3 main.py --file="sample.mp4" --title="Sample Movie" --description="This is a sample movie." --category="10" --privacyStatus="private"
```

## 注意事項

このスクリプトを使用する前に、`client_secrets.json`ファイルを正しく設定し、YouTube Data APIを有効にする必要があります。

## ライセンス

このプロジェクトはオープンソースであり、任意の用途で自由に使用できます。

このコードが役立つことを願っています！何か問題があれば、気軽にフィードバックしてください。
