---
title: Lemmy対応
date: 2023-03-14
categories: 機能
---

オープンソースのリンクアグリゲータ、[Lemmy](https://join.lemmy.ml/)に対応しています。

## リンクアグリゲータとは？

国内の同種のサービスとしては、[はてなブックマーク](https://b.hatena.ne.jp/)（縮めて「はてブ」とも）が有名と思います。
リンクアグリゲータを使って、気になったサイトやページをブックマークできます。保管したブックマークは、個人的に溜め込むもよし、積極的に公開するもよし。
リンクアグリゲータとは、そんな、ネットワーク対応のブックマークサービスです。

## どんなことが出来る？

Lemmyは、Misskeyのようなコミュニティ指向が、はてブ以上に強いリンクアグリゲータです。
Lemmyとダイスキーを連携させれば、それ以後、「お気に入り」の写しをMisskeyだけでなくLemmyにも残せる様になります。

私は、ダイスキー/[デルムリン丼](https://mastodon.delmulin.com/)以外に2つのサーバーを管理しています。
その全てがLemmyと紐づけられており、「お気に入り」（Mastodonでは「ブックマーク」）操作を行うとLemmyに集約されるようになっています。

## Lemmyサーバーを選ぶ

国内のLemmyサーバーは多くないようです。

- [鴉は拠り所について語り合う](https://lm.korako.me/)

ダイスキーでは、[鴉は拠り所について語り合う](https://lm.korako.me/)の利用をお勧めしています。これ以降の説明も、このサーバーを利用するものとして進めます。
まずは、[鴉は拠り所について語り合う](https://lm.korako.me/)で[アカウントを登録](https://lm.korako.me/login)してください。（以下）

{% asset_img account.png %}

## 個人用コミュニティ

ブックマークの保存先となる、個人用の[コミュニティを作成](https://lm.korako.me/create_community)してください。
ダイスキーで「お気に入り」操作を行うと、このLemmyコミュニティにもブックマークが溜まっていきます。

{% asset_img community.png %}

個人用コミュニティとは、何だか矛盾した響きですが。

また、 __コミュニティの「名前」を「ユーザー名」と同じものにしない様に__ 注意してください。Misskeyとの連携機能が全て誤動作します。
例えば、`pooza`というユーザーの個人用コミュニティとして`pooza`という名前のコミュニティを作ることは避け、`pooza1`などの別の名前で登録する様にしてください。

## ダイスキーからLemmyに接続

[モロヘイヤHOME](https://misskey.delmulin.com/mulukhiya)を初めて利用する方は、最初に[トークンの登録](https://misskey.delmulin.com/mulukhiya/app/token)を行ってください。
もし済んでいたら、[環境設定](https://misskey.delmulin.com/mulukhiya/app/config)仮面から設定を行います。

{% asset_img mulukhiya1.png %}

設定する項目は以下の3つ。

- __URL__ ： [鴉は拠り所について語り合う](https://lm.korako.me/)のURL、`https://lm.korako.me` を指定。
- __ユーザーID__ ：アカウント登録に使用したユーザーID、またはメールアドレス。
- __パスワード__ ：同、パスワード。

`更新`ボタンを押下。入力に誤りがなければ、保存先コミュニティが選択できるようになります。
__コミュニティ選択まで行わなければ設定は完了しません__ ので、ご注意下さい。

{% asset_img mulukhiya2.png %}

コミュニティを選択して、もう一度`更新`ボタンを押下。
ここまでの設定で、ダイスキーで保存した「お気に入り」がLemmyにも残せるようになります。
