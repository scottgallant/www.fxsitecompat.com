---
title: "Initializer in `for-of`/`in` loop head declaration is no longer allowed"
date: "2015-04-27T13:17:23-04:00"
categories: ["javascript"]
tags: []
versions: ["40"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=748550": "Bug 748550 - Remove InitialiserNoIn[opt] from ... in for(var ... in obj) to help simplify ES6"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1164741": "Bug 1164741 - Add back partial support for |for (var i = 0 in obj);| syntax, ignoring the initializer rather than failing on it"
---
Previously, the [`for...in`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in) and [`for...of`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of) statements could have an initializer in the loop head declaration, like `for (var/let/const x = ... in/of ...)`. This syntax had incorrectly been permitted by ECMAScript 1 to 5 but has been removed from ECMAScript 6. Firefox now ignores such initializers, so `for (var i = 0 in array)`, for example, will be parsed as `for (var i in array)`.
