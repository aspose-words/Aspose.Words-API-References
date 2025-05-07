---
title: PageSetup.bottomMargin property
linktitle: bottomMargin property
articleTitle: bottomMargin property
second_title: Aspose.Words for Node.js
description: "PageSetup.bottomMargin property. Returns or sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text."
type: docs
weight: 80
url: /nodejs-net/aspose.words/pagesetup/bottomMargin/
---

## PageSetup.bottomMargin property

Returns or sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text.


```js
get bottomMargin(): number
```

### Examples

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.pageSetup.paperSize = aw.PaperSize.Legal;
builder.pageSetup.orientation = aw.Orientation.Landscape;
builder.pageSetup.topMargin = aw.ConvertUtil.inchToPoint(1.0);
builder.pageSetup.bottomMargin = aw.ConvertUtil.inchToPoint(1.0);
builder.pageSetup.leftMargin = aw.ConvertUtil.inchToPoint(1.5);
builder.pageSetup.rightMargin = aw.ConvertUtil.inchToPoint(1.5);
builder.pageSetup.headerDistance = aw.ConvertUtil.inchToPoint(0.2);
builder.pageSetup.footerDistance = aw.ConvertUtil.inchToPoint(0.2);

builder.writeln("Hello world!");

doc.save(base.artifactsDir + "PageSetup.pageMargins.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

