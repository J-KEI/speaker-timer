# Speaker Timer

セッション登壇者向けのブラウザベース・フルスクリーンタイマー。
ビルド不要の単一HTMLファイルのみで動作します。

公開URL：https://speakertimer.static.jp/

## 機能

- カウントダウン形式（MM:SS）
- 開始前に持ち時間（分・秒）を画面上で設定（デフォルト：18分）
- 「全画面表示」「ウィンドウ表示」の2種類の開始方法
- 残り時間が指定時間以下になると文字色を変更（デフォルト：残り3分で黄色、オン/オフ可）
- 持ち時間経過後は自動でカウントアップに切り替わり、背景が白と黒で1秒ごとに点滅（文字色のデフォルト：赤）
- 背景色・文字色・警告時/超過時の文字色を「詳細設定（色）」で変更可能
- Arial Bold による大きく見やすい表示
- 画面下部の操作ボタン（マウスホバー時のみ表示）
  - カウント中：一時停止
  - 一時停止中：再開 / 時間をリセット / 設定に戻る
- キーボードショートカット
  - `Space`：カウント開始 / 停止
  - `R`：時間をリセット（一時停止中のみ）
  - `S`：設定画面に戻る（一時停止中のみ）
  - `Esc`：全画面表示を終了（ブラウザ標準機能）

## ローカルでの開発・確認

ビルドツール不要。`index.html` をブラウザで直接開くだけで動作します。

VSCode を使う場合は [Live Server 拡張機能](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
の利用を推奨します（`.vscode/extensions.json` に推奨設定済み）。

```bash
# 拡張機能を使わない場合の簡易サーバー例
npx serve .
```

## デプロイ（XServer Statics）

XServer Statics の GitHub 連携により、
`main` ブランチに push すると https://speakertimer.static.jp/ へ自動デプロイされます。
ビルドステップは無く、リポジトリ直下がそのまま公開されます。

## ディレクトリ構成

```
speaker-timer/
├── index.html              # タイマー本体（単一ファイル完結）
├── .vscode/                # VSCode 推奨設定
├── .editorconfig
├── .gitignore
├── LICENSE
├── README.md
└── CLAUDE.md                # Claude Code 向けプロジェクトコンテキスト
```

## ライセンス

MIT License（`LICENSE` 参照）
