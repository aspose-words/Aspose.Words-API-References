---
title: PageSetup.pageHeight property
linktitle: pageHeight property
articleTitle: pageHeight property
second_title: Aspose.Words for Node.js
description: "PageSetup.pageHeight property. Returns or sets the height of the page in points."
type: docs
weight: 310
url: /nodejs-net/aspose.words/pagesetup/pageHeight/
---

## PageSetup.pageHeight property

Returns or sets the height of the page in points.


```js
get pageHeight(): number
```

### Examples

Shows how to insert an image, and use it as a watermark.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert the image into the header so that it will be visible on every page.
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
let shape = builder.insertImage(base.imageDir + "Transparent background logo.png");
shape.wrapType = aw.Drawing.WrapType.None;
shape.behindText = true;

// Place the image at the center of the page.
shape.relativeHorizontalPosition = aw.Drawing.RelativeHorizontalPosition.Page;
shape.relativeVerticalPosition = aw.Drawing.RelativeVerticalPosition.Page;
shape.left = (builder.pageSetup.pageWidth - shape.width) / 2;
shape.top = (builder.pageSetup.pageHeight - shape.height) / 2;

doc.save(base.artifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

