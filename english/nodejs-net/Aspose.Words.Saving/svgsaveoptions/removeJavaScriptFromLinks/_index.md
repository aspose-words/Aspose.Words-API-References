---
title: SvgSaveOptions.removeJavaScriptFromLinks property
linktitle: removeJavaScriptFromLinks property
articleTitle: removeJavaScriptFromLinks property
second_title: Aspose.Words for Node.js
description: "SvgSaveOptions.removeJavaScriptFromLinks property. Specifies whether JavaScript will be removed from links"
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/svgsaveoptions/removeJavaScriptFromLinks/
---

## SvgSaveOptions.removeJavaScriptFromLinks property

Specifies whether JavaScript will be removed from links.
Default is ``false``.
If this option is enabled, all links containing JavaScript will be replaced with "javascript:void(0)".



```js
get removeJavaScriptFromLinks(): boolean
```

### Examples

Shows how to remove JavaScript from the links (svg).

```js
let doc = new aw.Document(base.myDir + "JavaScript in HREF.docx");

let saveOptions = new aw.Saving.SvgSaveOptions();
saveOptions.removeJavaScriptFromLinks = true;

doc.save(base.artifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SvgSaveOptions](../)

