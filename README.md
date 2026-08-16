# public-pages

静的 HTML の公開置き場。GitHub Pages で配信している。

- 公開 URL: https://koshiosaki.github.io/public-pages/
- 反映: `main` に push すると GitHub Actions が自動デプロイ（数十秒〜1分）

## 使い方

1. HTML をカテゴリ別ディレクトリに置く（例: `madamisu/xxx.html`）
2. `index.html` にリンクを1行追加する
3. commit して push

外部 CDN に依存しない自己完結 HTML を推奨（1ファイルで完結させる）。

## 注意

- **public repo**。置いたものは誰でも見られる。
- 検索に載せたくないページは `<head>` に以下を入れる:
  ```html
  <meta name="robots" content="noindex,nofollow">
  ```
- Notion に貼る場合は raw HTML ではなく、公開 URL を `/embed` で埋め込む。
