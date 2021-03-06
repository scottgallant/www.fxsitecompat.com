---
title: "Page Visibility API has been unprefixed"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom"]
tags: []
versions: ["18"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=812086": "Bug 812086 – Unprefix Page Visibility API"
---
The prefixed `mozvisibilitychange` event and the `mozHidden`, `mozVisibilityState` properties of the [Page Visibility API](https://developer.mozilla.org/en-US/docs/Web/Guide/User_experience/Using_the_Page_Visibility_API) are now deprecated. The unprefixed [`visibilitychange`](https://developer.mozilla.org/en-US/docs/Web/Reference/Events/visibilitychange) event and the [`hidden`](https://developer.mozilla.org/en-US/docs/Web/API/document.hidden), [`visibilityState`](https://developer.mozilla.org/en-US/docs/Web/API/document.visibilityState) properties should be used instead.
