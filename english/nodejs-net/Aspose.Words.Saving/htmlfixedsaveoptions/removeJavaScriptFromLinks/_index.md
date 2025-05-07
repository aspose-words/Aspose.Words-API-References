---
title: HtmlFixedSaveOptions.removeJavaScriptFromLinks property
linktitle: removeJavaScriptFromLinks property
articleTitle: removeJavaScriptFromLinks property
second_title: Aspose.Words for Node.js
description: "HtmlFixedSaveOptions.removeJavaScriptFromLinks property. Specifies whether JavaScript will be removed from links"
type: docs
weight: 140
url: /nodejs-net/aspose.words.saving/htmlfixedsaveoptions/removeJavaScriptFromLinks/
---

## HtmlFixedSaveOptions.removeJavaScriptFromLinks property

Specifies whether JavaScript will be removed from links.
Default is ``false``.



```js
get removeJavaScriptFromLinks(): boolean
```

### Remarks

If this option is enabled, all links containing JavaScript (e.g., links with "javascript:" in the href attribute)
will be replaced with "javascript:void(0)". This can help prevent potential security risks, such as XSS attacks.


### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

