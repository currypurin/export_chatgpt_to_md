# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

ChatGPTの公式データエクスポート（conversations.json）をMarkdownファイルに変換するブラウザアプリ。サーバー不要、完全クライアントサイド処理。

## Architecture

単一HTMLファイル構成（`docs/index.html`）:

- **UI**: ファイル選択（ドラッグ&ドロップ対応）、モード選択、変換ボタン
- **外部依存**: JSZip（CDN）のみ

主要なJavaScript関数:
- `loadConversations()`: JSON読み込み
- `extractLinearMessages()`: ChatGPTのmappingツリー構造から線形メッセージチェーンを再構築
- `renderConvToMd()`: 会話をMarkdown形式に変換（YAMLフロントマター付き）
- `safeFilename()`: ファイル名のサニタイズ

## GitHub Pages

`docs/` フォルダから配信。Settings > Pages で設定。
