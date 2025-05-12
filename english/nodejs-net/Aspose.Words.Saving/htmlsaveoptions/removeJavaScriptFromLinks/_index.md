---
title: HtmlSaveOptions.removeJavaScriptFromLinks property
linktitle: removeJavaScriptFromLinks property
articleTitle: removeJavaScriptFromLinks property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.removeJavaScriptFromLinks property. Specifies whether JavaScript will be removed from links"
type: docs
weight: 410
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/removeJavaScriptFromLinks/
---

## HtmlSaveOptions.removeJavaScriptFromLinks property

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
* class [HtmlSaveOptions](../)

