---
title: Slack互換webhook
date: 2021-03-17
categories: 機能
---

ボットや自動投稿を作る方の便宜の為、webhookを提供しています。
仕様上は、[Slack Incoming Webhook](https://slack.com/intl/ja-jp/help/articles/115005265063-Slack-%E3%81%A7%E3%81%AE-Incoming-Webhook-%E3%81%AE%E5%88%A9%E7%94%A8)のサブセットです。簡単なSlackボットなら、既存のものを無改造でデルムリン丼対応にできるかもしれません。

## 利用の手順

拙作の自動のRSSフィードを[IFTTT](https://ifttt.com/)を使ってwebhookに転送する例で説明します。

### RSS/Atomフィードを調べる

以下、東映アニメーションの[プリキュア公式サイト](https://www.toei-anim.co.jp/tv/precure/)の新着情報のRSSフィードです。

https://precure.b-shock.org/feed/v1.0/site/toei

### webhookのURLを調べる

[モロヘイヤHOME](https://mstdn.delmulin.com/mulukhiya/app/webhook)で、webhookのURLを調べられます。
[トークンの登録](https://mstdn.delmulin.com/mulukhiya/app/token)をまだ行っていなかったら、最初に実行してください。おなじみの画面が出てきますので、指示に従ってください。

トークンが登録済みなら、「環境設定」画面にwebhookのURLがあるはずです。

{% asset_img 手順5.png %}

ここまでで事前準備は終了。このあと実際に、[IFTTT](https://ifttt.com/)で登録を行っていきます。

### トリガー

[IFTTT](https://ifttt.com/)の画面上で、[Create](https://ifttt.com/create)を実行します。
`rss` 等の検索語で __RSS Feed__ トリガーを検索し、これを選択。

{% asset_img 手順1.png %}

そして、先ほどのフィードURLを設定。
AtomフィードもRSSの一種とみなされ、登録可能です。今さら野暮を言う様ですが。

{% asset_img 手順2.png %}

### アクション

`webhook` 等の検索語で __Webhooks__ アクションを検索し、これを選択。

{% asset_img 手順3.png %}

設定内容は、こんな感じ。

{% asset_img 手順4.png %}

URLは、先ほど調べたwebhookのURL。
Bodyには、たとえば以下の様なJSONを。

```json
{"text":"<<<{{EntryTitle}}>>>\n<<<{{EntryUrl}}>>>"}
```

保存して実行しましょう。以上です。
