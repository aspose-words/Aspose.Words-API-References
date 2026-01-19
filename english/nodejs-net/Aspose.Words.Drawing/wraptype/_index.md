---
title: WrapType enumeration
linktitle: WrapType enumeration
articleTitle: WrapType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.WrapType enumeration. Specifies how text is wrapped around a shape or picture."
type: docs
weight: 540
url: /nodejs-net/aspose.words.drawing/wraptype/
---

## WrapType enumeration

Specifies how text is wrapped around a shape or picture.


### Members

| Name | Description |
| --- | --- |
| None | No text wrapping around the shape. The shape is placed behind or in front of text. |
| Inline | The shape remains on the same layer as text and treated as a character. |
| TopBottom | The text stops at the top of the shape and restarts on the line below the shape. |
| Square | Wraps text around all sides of the square bounding box of the shape. |
| Tight | Wraps tightly around the edges of the shape, instead of wrapping around the bounding box. |
| Through | Same as Tight, but wraps inside any parts of the shape that are open. |

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

Shows how to insert a floating image to the center of a page.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
let shape = builder.insertImage(base.imageDir + "Logo.jpg");
shape.wrapType = aw.Drawing.WrapType.None;
shape.behindText = true;
shape.relativeHorizontalPosition = aw.Drawing.RelativeHorizontalPosition.Page;
shape.relativeVerticalPosition = aw.Drawing.RelativeVerticalPosition.Page;
shape.horizontalAlignment = aw.Drawing.HorizontalAlignment.Center;
shape.verticalAlignment = aw.Drawing.VerticalAlignment.Center;

doc.save(base.artifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### See Also

* module [Aspose.Words.Drawing](../)
* property [ShapeBase.wrapType](../shapebase/wrapType/)

