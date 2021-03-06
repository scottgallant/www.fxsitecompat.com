---
title: "RC4 is now completely disabled by default"
date: "2015-10-20T14:47:00-07:00"
categories: ["privacy-security"]
tags: []
versions: ["44"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=999544": "Bug 999544 - RC4 Considered Harmful: Disable use of RC4 completely (RFC 7465)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1201025": "Bug 1201025 - Disable fallback whitelist by default, in all releases"
    "https://blog.mozilla.org/security/2015/09/11/deprecating-the-rc4-cipher/": "Deprecating the RC4 Cipher"
    "https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion": "Intent to ship: RC4 disabled by default in Firefox 44"
---
Mozilla and other major browser vendors have agreed to stop supporting the insecure RC4 cipher suites, [deprecated since Firefox 36](https://www.fxsitecompat.com/en-CA/docs/2014/rc4-support-has-been-deprecated/), in early <time datetime="2016">2016</time>.

As per the [deprecation plan](https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion), Firefox 44 has disabled the [whitelist](https://dxr.mozilla.org/mozilla-central/source/security/manager/ssl/IntolerantFallbackList.inc) that allowed certain sites to use RC4, therefore users will see the [Untrusted Connection](https://support.mozilla.org/en-US/kb/connection-untrusted-error-message) error message on any sites with RC4 enabled. Web servers must be upgraded as soon as possible to use stronger cipher suites.
