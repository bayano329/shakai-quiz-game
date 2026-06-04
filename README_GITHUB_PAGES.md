# 高校受験社会クイズアプリ 公開用ファイル

GitHub Pagesで公開するためのファイル一式です。

## 現在収録している問題

- 地理：700問
- 歴史：500問
- 合計：1200問

## リポジトリ直下に置くファイル

```text
/
├─ index.html
├─ geography.json
├─ history.json
├─ .nojekyll
├─ README_GITHUB_PAGES.md
├─ manifest.json
└─ docs/
   ├─ geography_all_001_700.md
   ├─ geography_duplicate_report.md
   ├─ history_all_001_500.md
   ├─ history_check_report.md
   └─ history_duplicate_report.md
```

## GitHub Pagesでの設定

1. 上記ファイルをGitHubリポジトリ直下にアップロードする
2. `Settings` → `Pages` を開く
3. `Source` を `Deploy from a branch` にする
4. `Branch` を `main`、フォルダを `/root` にする
5. `Save` を押す
6. 表示されたURLを開く

## 注意

- `index.html`、`geography.json`、`history.json` は必ず同じ階層に置いてください。
- 画面上にはVer表記を出していません。
- トップ説明文は選択中の科目名のみを表示します。
- 学習記録と苦手問題は科目ごとに保存されます。

## 今後の公民追加時の想定

公民を追加する場合は、以下のように `civics.json` を追加し、`index.html` の `DATASETS` に1行追加します。

```text
/
├─ index.html
├─ geography.json
├─ history.json
└─ civics.json
```
