# 高校受験社会クイズアプリ 公開用Ver5

このフォルダは GitHub Pages で公開するための最小構成です。

## 公開に必要なファイル

- `index.html`  
  公開用トップページです。ブラウザで最初に開かれるファイルです。
- `geography.json`  
  地理700問のアプリ用データです。`index.html` と同じ階層に置いてください。
- `.nojekyll`  
  GitHub PagesでJekyll処理を無効化するための空ファイルです。
- `docs/`  
  管理用資料です。公開に必須ではありませんが、問題確認・重複確認のために残しています。

## GitHub Pagesでの配置

リポジトリ直下に以下のように配置してください。

```text
/
├─ index.html
├─ geography.json
├─ .nojekyll
└─ docs/
   ├─ geography_all_001_700.md
   ├─ geography_duplicate_report.md
   └─ index_ver4_geography_backup.html
```

## GitHub側の設定

1. GitHubでリポジトリを作成する
2. 上記ファイルをリポジトリ直下にアップロードする
3. `Settings` → `Pages` を開く
4. `Build and deployment` の `Source` で `Deploy from a branch` を選ぶ
5. `Branch` を `main`、フォルダを `/root` にして保存する
6. 数分後に表示されるURLへアクセスする

## 注意

- `index.html` と `geography.json` は必ず同じ階層に置いてください。
- `index.html` のファイル名は小文字で固定してください。
- ローカルで直接 `index.html` を開くと、ブラウザの制限で `geography.json` を読み込めない場合があります。
  その場合はローカルサーバーを使って確認してください。

```bash
cd 公開用フォルダ
python -m http.server 8000
```

その後、ブラウザで `http://localhost:8000/` を開いて確認します。

## 今後の拡張方針

歴史・公民を追加する場合は、以下のようにJSONを増やす設計にできます。

```text
/
├─ index.html
├─ geography.json
├─ history.json
└─ civics.json
```

Ver5では問題データをHTMLに直接埋め込まず、外部JSONとして読み込む形にしています。
そのため、今後1300〜1500問規模になっても管理しやすくなります。
