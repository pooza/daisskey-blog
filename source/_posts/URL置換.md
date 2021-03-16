---
title: URL置換
date: 2021-03-17
categories: 機能
---

トゥート本文に書かれたURLについて、以下の置換を行います。

## 短縮URLを元に戻す
- `t.co`等、短縮URLには本来のURLを隠す性質があります。用心深いメンバーは、そのURLを開くこと躊躇するでしょう。これを元に戻します。
- 詳細: [ShortenedURLHandler](https://github.com/pooza/mulukhiya-toot-proxy/wiki/ShortenedURLHandler)

## 日本語を含んだURLを正しいものに置換
- 日本語を含んだURLは、[クライアント](/articles/クライアント)によっては、クリック/タップしても開くことが出来ない場合があります。同じ意味の日本語を含まない形式に置換すれば、どのクライアントでも開くことができる様になります。
- 詳細: [URLNormalizeHandler](https://github.com/pooza/mulukhiya-toot-proxy/wiki/URLNormalizeHandler)

## HTMLソース内にCanonical指定を含むページでは、そのURLに置換
- 複数のURLで呼び出せて、どのURLでアクセスしても同じ内容になるページがよくあります。この場合、サービス側は、「本来のURLはどれか」を指定している場合があります。
- 詳細: [CanonicalHandler](https://github.com/pooza/mulukhiya-toot-proxy/wiki/CanonicalHandler)

## Amazonの商品URLを短く
- Amazonの商品URLは、日本語を含んだ非常に長いものになりがちです。そのままでは扱いづらいですが、縮めることが可能です。
- 詳細: [AmazonASINHandler](https://github.com/pooza/mulukhiya-toot-proxy/wiki/AmazonASINHandler)

## iTunes StoreのURLを短く
- iTunes StoreのURLも、同様に縮めることが可能です。
- 詳細: [ItunesURLHandler](https://github.com/pooza/mulukhiya-toot-proxy/wiki/ItunesURLHandler)

