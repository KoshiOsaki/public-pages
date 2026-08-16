# public-pages

静的 HTML の公開置き場。GitHub Pages で配信している。

- 公開 URL: https://koshiosaki.github.io/public-pages/
- 配信: `main` ブランチ root からの GitHub Pages（legacy branch build）。push すると数十秒〜1分で反映

## 使い方

Claude Code から `publish-page` skill（`~/dotfiles/claude/skills/publish-page/`）で公開する。
「htmlにして公開」「このページ公開して」で起動する。

手動でやる場合:

1. HTML をカテゴリ別ディレクトリに置く（例: `madamisu/xxx.html`）
2. `index.html` にリンクを1行追加する
3. commit して push

外部 CDN に依存しない自己完結 HTML を推奨（1ファイルで完結させる）。
他 repo からの symlink は張らない（GitHub Pages が解決できず壊れる）。コピーで運用する。

## 注意

- **public repo**。置いたものは誰でも見られる。
- 検索に載せたくないページは `<head>` に以下を入れる:
  ```html
  <meta name="robots" content="noindex,nofollow">
  ```
- Notion に貼る場合は raw HTML ではなく、公開 URL を `/embed` で埋め込む。
