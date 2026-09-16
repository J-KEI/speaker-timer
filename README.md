# Speaker Timer

セッション登壇者向けのブラウザベース・フルスクリーンタイマー。
ビルド不要の単一HTMLファイルのみで動作します。

## 機能

- カウントダウン形式（MM:SS）
- 開始前に持ち時間（分・秒）を画面上で設定
- 背景色・文字色をカラーピッカーで設定可能（デフォルト：黒背景 / 白文字）
- Arial Bold による大きく見やすい表示（全画面表示）
- 持ち時間経過後は自動でカウントアップに切り替わり、背景が赤で1秒ごとに点滅
- キーボードショートカット
  - `Space`：一時停止 / 再開
  - `R`：設定画面に戻る
  - `Esc`：全画面表示を終了（ブラウザ標準機能）

## ローカルでの開発・確認

ビルドツール不要。`index.html` をブラウザで直接開くだけで動作します。

VSCode を使う場合は [Live Server 拡張機能](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
の利用を推奨します（`.vscode/extensions.json` に推奨設定済み）。

```bash
# 拡張機能を使わない場合の簡易サーバー例
npx serve .
```

## デプロイ（GitHub Pages）

`main` ブランチに push すると `.github/workflows/deploy.yml` により
GitHub Pages へ自動デプロイされます。

初回のみ、リポジトリの `Settings > Pages > Build and deployment` で
**Source: GitHub Actions** を選択してください。

## ディレクトリ構成

```
speaker-timer/
├── index.html              # タイマー本体（単一ファイル完結）
├── .github/workflows/      # GitHub Pages 自動デプロイ
├── .vscode/                # VSCode 推奨設定
├── .editorconfig
├── .gitignore
├── LICENSE
├── README.md
└── CLAUDE.md                # Claude Code 向けプロジェクトコンテキスト
```

## ライセンス

MIT License（`LICENSE` 参照）
