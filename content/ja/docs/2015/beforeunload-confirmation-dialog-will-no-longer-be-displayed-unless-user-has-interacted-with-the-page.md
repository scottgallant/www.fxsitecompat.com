---
title: "`beforeunload` 確認ダイアログはユーザがページ上で操作をしない限り表示されなくなりました"
date: "2015-09-29T10:25:00-04:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=636905": "Bug 636905 - Don't allow onbeforeunload dialog unless I have interacted with the page"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=578828": "Bug 578828 - Default to not allowing onbeforeunload dialogs"
aliases:
    - "/docs/2015/beforeunload-event-will-no-longer-be-fired-unless-user-has-interacted-with-the-page/"
    - "/docs/2015/beforeunload-dialog-will-no-longer-be-displayed-unless-user-has-interacted-with-the-page/"
---
[`beforeunload`](https://developer.mozilla.org/ja/docs/Web/Events/beforeunload) イベントは、ポップアップ広告を含め、Web ページがユーザによって閉じられるのを妨げる目的で乱用されることがしばしばあります。Firefox は、ユーザがページ上でクリック、タッチ、スクロール、文字入力といった何らかのインタラクションを起こさない限り、`beforeunload` イベントハンドラの戻り値を無視し、確認ダイアログを表示せずにページ遷移を強制するようになりました。

また、すべての `beforeunload` ダイアログを初期設定で不許可とする計画もあるため、Web 開発者にはページ遷移を確認するためにこの種類のイベントを使用するのを避けるよう推奨します。Web ページやアプリは、[Web Storage API](https://developer.mozilla.org/ja/docs/Web/API/Web_Storage_API) や [IndexedDB API](https://developer.mozilla.org/ja/docs/Web/API/IndexedDB_API) でローカルに、あるいは [Ajax](https://developer.mozilla.org/ja/docs/Ajax) テクニックを使ってリモートにドラフト状態を保存することで、データ消失を防ぎつつユーザ体験を向上させることが可能です。

**更新**: このドキュメントの初期草稿は誤解を招く内容でした。ユーザがページ上でインタラクションを起こしていない場合でも `beforeunload` イベント自体が発動されることに変わりはありません。
