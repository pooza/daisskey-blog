---
title: モロヘイヤHOME
date: 2021-03-17
categories: 機能
---

![HOME](HOME.png)

モロヘイヤHOME
https://mstdn.delmulin.com/mulukhiya

## モロヘイヤHOMEとは？

デルムリン丼にいくつかの独自機能を実現しているツール「[モロヘイヤ](https://github.com/pooza/mulukhiya-toot-proxy)」の、各種管理機能をまとめた画面です。
モロヘイヤに対して、以下の操作を行えます。

- 環境設定
- 動作設定の確認
- webhookの作成
- [デフォルトハッシュタグ](/articles/delmulin) `#delmulin` へのリンク

## どこにある？
https://mstdn.delmulin.com/mulukhiya を直接開いてもよいですし、以下のオレンジ色の場所にあるリンクから開いてもよいです。

### 「上級者向けUI」（別名マルチカラム）の場合
![マルチカラム](multi.png)

### 通常UIの場合
![シングルカラム](single.png)

## 最初にやること
[アプリケーションの認証](https://mstdn.delmulin.com/mulukhiya/app/auth)を実行してください。
スマホアプリ（Subway Tooter / Tootle等）にアカウントを登録する時にも同様の画面が表示されますので、手順はご存知のことと思います。
最後に表示される「認証コード」（以下）をモロヘイヤに登録すれば、以後、「環境設定」「webhook」が利用できるようになります。
![認証コード](code.png)

## 環境設定
[アプリケーションの認証](https://mstdn.delmulin.com/mulukhiya/app/auth)を行ったあとであれば、[環境設定](https://mstdn.delmulin.com/mulukhiya/app/config)画面を開くことが出来ます。

ここから設定できる項目はいくつかありますが、「固定タグ」が有用と思います。
基本的には[実況用タグを設定する](/articles/実況用タグを設定する)機能と同じものですが、このメニューはMastodonの本体改造によって実装されている為、将来に渡って利用可能であることを必ずしも保証できません。（可能性は低いですが、今後Mastodonに追加される機能と共存できなくなるかもしれません）

[環境設定](https://mstdn.delmulin.com/mulukhiya/app/config)画面はモロヘイヤの機能である為、今後廃止されることはありません。これは保険として作られた機能でもあります。
![固定タグ](tags.png)
