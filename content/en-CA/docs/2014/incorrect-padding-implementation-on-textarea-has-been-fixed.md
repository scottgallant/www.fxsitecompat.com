---
title: "Incorrect `padding` implementation on `<textarea>` has been fixed"
date: "2014-02-07T11:57:09-05:00"
categories: ["css"]
tags: []
versions: ["29"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=157846": "Bug 157846 – Incorrect implementation of padding on textarea elements (scrollbars/resizer wrongly positioned)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1012202": "Bug 1012202 – eBay Messages: textarea is expanded while typing due to the scrollHeight change with Firefox 29"
---
Firefox's incorrect implementation of [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding) on the [`<textarea>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea) element has been fixed to resolve a longstanding browser compatibility issue, as [this screenshot shows](https://bug157846.bugzilla.mozilla.org/attachment.cgi?id=784647). Now `padding` spaces are added inside the scrollbar and resizer controls, instead of outside, to match with the CSS spec and other browsers' behaviour.

The `padding` will be included in the [`clientWidth`](https://developer.mozilla.org/en-US/docs/Web/API/Element.clientWidth), [`clientHeight`](https://developer.mozilla.org/en-US/docs/Web/API/Element.clientHeight), [`scrollWidth`](https://developer.mozilla.org/en-US/docs/Web/API/Element.scrollWidth) and [`scrollHeight`](https://developer.mozilla.org/en-US/docs/Web/API/Element.scrollHeight) properties of the element. A side effect of this change has been found on *eBay* where the height of a message textarea is programmatically expanded while typing.
