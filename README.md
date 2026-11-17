# 玄界灘 — 筑前海の海中

Three.js を用いた玄界灘・筑前海（藻場・沈み瀬・磯焼け）の 3D 水中生態系ビューワーです。

## 構成ファイル

- `index.html`: Three.js（`unpkg.com/three@0.160.0`）ベースの単一エントリ HTML・カスタムシェーダー群
- `assets/bio/`: 生物切り抜きテクスチャ（24種 PNG）および 3D 厚みプロファイル `profiles.json`
- `assets/tex/`: 海底砂地・岩礁用 PBR テクスチャ（`coast_sand_04_*`, `aerial_rocks_02_*`）
- `.nojekyll`: GitHub Pages での静的ファイル配信をそのまま有効化する設定ファイル

## 公開・閲覧方法

### GitHub Pages で公開する場合
1. GitHub 上でリポジトリを作成し、このディレクトリの内容を `main` ブランチへプッシュします。
2. リポジトリの **Settings > Pages** から Branch に `main` / `/ (root)` を選択して保存すると、静的ページとしてそのまま公開されます。

### ローカルで確認する場合
ES Module および JSON / テクスチャの `fetch` 読み込みのため、ローカル HTTP サーバー経由で開きます。

```bash
python3 -m http.server 8124 --bind 127.0.0.1
```

ブラウザで `http://127.0.0.1:8124/` を開いて閲覧できます。
