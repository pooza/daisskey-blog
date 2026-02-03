# daisskey-blog

ダイスキーBlogのリポジトリです。GitHub Pages（GitHub Actions）でビルド・公開します。

## 全体像
- 記事: `/_posts/` に配置（Jekyll 標準）
- 画像: `/images/` に集約（記事フォルダ名で整理）
- 生成物: `/_site/` に出力（公開対象）
- URL: `/articles/:title/` 形式
- カテゴリ一覧: `/categories/`
- ビルド/公開: `.github/workflows/pages.yml`

## 記事の書き方
### ファイル名
```
_posts/2026-01-30-記事スラッグ.md
```

### front-matter（最小）
```
---
title: 記事タイトル
date: 2026-01-30
categories: カテゴリ名
---
```

### リンク（記事同士）
```
[リンクテキスト]({{ "/articles/記事スラッグ/" | relative_url }})
```

### 画像
```
![]({{ "/images/記事名/画像.png" | relative_url }})
```

## 普段行う操作
### ローカルプレビュー
```
bundle exec jekyll serve --livereload
```
ブラウザ: `http://127.0.0.1:4000/`

### ビルド確認
```
bundle exec jekyll build
```

## GitHub Pages / Actions
- `dev` では build のみ
- `main` で deploy

## Ruby/Jekyll 環境
```
rbenv local 3.3.10
bundle install
```
