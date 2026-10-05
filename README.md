# AIで作って海外販売！日本風ポスター完全ガイド（Instagramリール特典ページ）

ビルド不要の静的サイト（HTML / CSS / JavaScript）です。サーバー・データベース・APIキーは使いません。

```text
index.html   ページ本体（文章・プロンプトはここが単一の源）
style.css    見た目（色は先頭の :root で変更）
script.js    コピー・売上計算・完了チェック・固定ボタン（設定値は先頭の定数）
assets/      画像（ポスター3枚、CTAバナー、教科書の目次画像、favicon）
docs/        要件定義書・進捗管理表
```

## ローカルで確認する

`index.html` をブラウザで開く、またはこのフォルダで次を実行します。

```bash
python3 -m http.server 8000
```

→ http://localhost:8000 を開きます。

## GitHub Pages で公開する

1. GitHub のリポジトリ → **Settings → Pages**
2. **Source** を「Deploy from a branch」にし、ブランチ `main`、フォルダ `/ (root)` を選んで **Save**
3. 数分後、`https://mion-ai-mama.github.io/japanese-poster-etsy-tokuten/` で公開されます

## LINEのURLを変える

`script.js` 先頭の `LINE_URL` を書き換えます。空にすると、LINEへのボタンはすべて非表示になります（架空のリンクは出しません）。

## 画像を差し替える

`assets/images/` の次のファイルを、同じ名前で置き換えます。

| ファイル | 場所 |
|---|---|
| `poster-sakura-fuji.jpg` | ファーストビュー（1枚目）／SNSシェア用の画像（OGP） |
| `poster-kyoto-machiya.jpg` | ファーストビュー（2枚目） |
| `poster-goldfish.jpg` | ファーストビュー（3枚目） |
| `cta-banner.png` / `cta-textbook-contents.png` | CTA（教科書のバナー・目次） |

縦長（3:4）の画像がきれいに収まります。

## 内容について

- Etsyの手数料・出品ルールは、2026年10月5日に公式ページで確認した内容です。変更される可能性があるため、公開後も定期的に公式情報と見比べてください。
- 「月20万円」は仮定の売上シミュレーションです。収益を保証するものではありません。
