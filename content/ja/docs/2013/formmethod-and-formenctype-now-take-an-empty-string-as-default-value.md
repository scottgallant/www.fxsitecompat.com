---
title: "`formMethod` と `formEnctype` が空文字列を既定値として取るようになりました"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: ["21"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=787095": "Bug 787095 – Update formMethod reflection to have the empty string as default value (and \'get\' as invalid value)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=839171": "Bug 839171 – Update formMethod reflection to have the empty string as default value (and \'get\' as invalid value)"
---
[`formMethod`](https://developer.mozilla.org/ja/docs/HTML/Element/Input#attr-formmethod)、[`formEnctype`](https://developer.mozilla.org/ja/docs/HTML/Element/Input#attr-formenctype) 両プロパティの HTML5 仕様が更新され、空文字列を既定値として取るようになりました。Firefox はこの変更に追従しました。
