---
title: "一部の Web フォントがより厳格なバリデーションのため表示されなくなる場合があります"
date: "2016-02-03T13:19:00-05:00"
categories: ["misc"]
tags: []
versions: ["44"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1244693": "Bug 1244693 - FF 44 fails to load some WOFF fonts"
---
Firefox 44 以降で、OpenType Sanitizer の新バージョンによるより厳密なバリデーションが行われるため、一部の Web フォントが拒絶される場合があります。仕様に反した OpenType レイアウトテーブルを含むフォントは描画されず、Web コンソールにそのエラーに関する警告が表示されます。

**更新**: *Nokia* を含め一部のサイトが影響を受けていることから、Firefox 45 以降、Beta、Release 両チャンネルではこのバリデーションは緩和されています。しかし、問題のあるフォントはいずれにしても置き換えられるべきです。
