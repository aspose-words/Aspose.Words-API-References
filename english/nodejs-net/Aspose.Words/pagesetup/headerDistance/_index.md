---
title: PageSetup.headerDistance property
linktitle: headerDistance property
articleTitle: headerDistance property
second_title: Aspose.Words for NodeJs
description: "PageSetup.headerDistance property. Returns or sets the distance (in points) between the header and the top of the page."
type: docs
weight: 170
url: /nodejs-net/aspose.words/pagesetup/headerDistance/
---

## PageSetup.headerDistance property

Returns or sets the distance (in points) between the header and the top of the page.


```js
get headerDistance(): number
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

