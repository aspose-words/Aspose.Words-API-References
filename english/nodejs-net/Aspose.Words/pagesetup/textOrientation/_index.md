---
title: PageSetup.textOrientation property
linktitle: textOrientation property
articleTitle: textOrientation property
second_title: Aspose.Words for NodeJs
description: "PageSetup.textOrientation property. Allows to specify [PageSetup.textOrientation](./) for the whole page"
type: docs
weight: 430
url: /nodejs-net/aspose.words/pagesetup/textOrientation/
---

## PageSetup.textOrientation property

Allows to specify [PageSetup.textOrientation](./) for the whole page.
Default value is [TextOrientation.Horizontal](../../textorientation/#Horizontal)



```js
get textOrientation(): Aspose.Words.TextOrientation
```

### Remarks

This property is only supported for MS Word native formats DOCX, WML, RTF and DOC.


### Examples

Shows how to set text orientation.

```js
let doc = new aw.Document();

let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

// Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
// to the right so that all left-to-right text now goes top-to-bottom.
let pageSetup = doc.sections.at(0).pageSetup;
pageSetup.textOrientation = aw.TextOrientation.Upward;

doc.save(base.artifactsDir + "PageSetup.SetTextOrientation.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

