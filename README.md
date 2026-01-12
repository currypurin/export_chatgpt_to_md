# ChatGPT to Markdown Converter

ChatGPTの **公式データエクスポート（conversations.json）** を、検索・保管しやすい **Markdown（.md）** に変換するWebアプリです。

> このプロジェクトは [pawaramorucha819/export_chatgpt_to_md](https://github.com/pawaramorucha819/export_chatgpt_to_md) をフォークし、ブラウザで動作するよう作り直したものです。

## 特徴

- ブラウザで完結（データはサーバーに送信されません）
- 変換モード
  - `per_month`：月ごと（YYYY-MM）に束ねて出力
  - `per_year`：年ごと（YYYY）に束ねて出力
  - `per_chat`：会話ごとに1ファイルで出力
- ZIPファイルでダウンロード

## 使い方

詳しい使い方は[こちらの記事](https://note.com/currypurin/n/n671c75f1eeb3)で説明しています。

### 1) ChatGPTからデータをエクスポートする

ChatGPTの設定から **Export data** を実行し、届いたZIPを解凍します。
解凍後、以下のファイルが含まれます：

- `conversations.json`

### 2) 変換する

1. [ChatGPT to Markdown Converter](https://currypurin.github.io/export_chatgpt_to_md/) にアクセス
2. `conversations.json` をドラッグ&ドロップ、または「ファイルを選択」
3. 出力モードを選択（per_month / per_year / per_chat）
4. 「変換してダウンロード」をクリック
5. ZIPファイルがダウンロードされる

## 出力例

### per_month（月ごとにまとめる）

```
chatgpt_md_per_month.zip
  2025-12_chatgpt_bundle.md
  2026-01_chatgpt_bundle.md
  ...
```

### per_year（年ごとにまとめる）

```
chatgpt_md_per_year.zip
  2025_chatgpt_bundle.md
  2026_chatgpt_bundle.md
  ...
```

### per_chat（会話ごとに分割）

```
chatgpt_md_per_chat.zip
  20260103_MyTitle_ab12cd34.md
  20251230_OtherTitle_ef56gh78.md
  ...
```

## プライバシー

- すべての処理はブラウザ内で完結します
- `conversations.json` のデータは外部に送信されません
- 変換結果に機密情報が含まれる場合があります。公開・共有時はご注意ください

## ソースコード

- [GitHub](https://github.com/currypurin/export_chatgpt_to_md)

## 免責

本ソフトウェアは MIT License の条件に基づき「現状のまま」提供され、いかなる保証もありません。利用により生じた損害について、著作者は責任を負いません。

## ライセンス

MIT License（`LICENCE` を参照）
