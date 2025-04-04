---
title: PageSetup.pageWidth property
linktitle: pageWidth property
articleTitle: pageWidth property
second_title: Aspose.Words for Node.js
description: "PageSetup.pageWidth property. Returns or sets the width of the page in points."
type: docs
weight: 340
url: /nodejs-net/aspose.words/pagesetup/pageWidth/
---

## PageSetup.pageWidth property

Returns or sets the width of the page in points.


```js
get pageWidth(): number
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

Shows how to insert a floating image, and specify its position and size.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertImage(base.imageDir + "Logo.jpg");
shape.wrapType = aw.Drawing.WrapType.None;

// Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
// as the shape's horizontal distance, in points, from the left side of the page. 
shape.relativeHorizontalPosition = aw.Drawing.RelativeHorizontalPosition.Page;

// Set the shape's horizontal distance from the left side of the page to 100.
shape.left = 100;

// Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
shape.relativeVerticalPosition = aw.Drawing.RelativeVerticalPosition.Page;
shape.top = 80;

// Set the shape's height, which will automatically scale the width to preserve dimensions.
shape.height = 125;

expect(shape.width).toEqual(125.0);

// The "Bottom" and "Right" properties contain the bottom and right edges of the image.
expect(shape.bottom).toEqual(shape.top + shape.height);
expect(shape.right).toEqual(shape.left + shape.width);

doc.save(base.artifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

