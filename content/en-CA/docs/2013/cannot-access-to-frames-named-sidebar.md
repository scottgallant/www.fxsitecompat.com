---
title: "Cannot access to frames named `sidebar`"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=888225": "Bug 888225 – firefox 22 breaks access to frames named \'sidebar\'"
---
Firefox 22 has broken access to the [`<frame>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frame) and [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe) elements named `sidebar`. This regression has been fixed in Firefox 23.
