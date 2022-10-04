---
title: Annict対応
date: 2022-10-05
categories: 機能
---

## 機能概要

- デルムリン丼のアカウントと[Annict](https://annict.jp)のアカウントの紐づけを行えます。
- [Annict](https://annict.jp)で、ダイ大や他のアニメの視聴記録を行うことができます。感想も書けますので、できるだけ書くとよいと思います。
- 1分以内に、視聴記録のまとめが投稿されます。
- 本文中に「ネタバレ」文字列を含むと、CWで投稿されます。
  - [デルムリン丼とは？](/articles/about)で書いた通り、現時点までの放送回に含まれないネタはCWにしてください。

## 設定の手順

### Annictに登録

- [Annict](https://annict.jp)のアカウントを持っていなければ、[登録](https://annict.jp/sign_up)を行う。

### モロヘイヤHOME

- [HOME](https://mstdn.delmulin.com/mulukhiya)を開く。
- その端末で初めて[HOME](https://mstdn.delmulin.com/mulukhiya)を利用する場合は、[トークンの登録](https://mstdn.delmulin.com/mulukhiya/app/token)を最初に行うこと。

### 環境設定画面

- トークンが登録済みの場合は、[環境設定](https://mstdn.delmulin.com/mulukhiya/app/config)画面へ。
- Annictの設定、「認証コードを取得」リンクをクリック。

{% asset_img HOME.png %}

- Annictへのリンクが開くので、指示に従う。最後に表示される「認証コード」を手元のメモアプリ等に控える。

{% asset_img Annict認証.png %}

- [モロヘイヤHOME](https://mstdn.delmulin.com/mulukhiya/app/config)に戻り、認証コードを貼り付けて「認証」ボタン。
- 「現在の設定」にAnnict関連の設定が加わったことを確認し、設定終了。

## 技術的な詳細

https://github.com/pooza/mulukhiya-toot-proxy/wiki/Annict%E5%AF%BE%E5%BF%9C
https://annict.jp/userland/projects/60
