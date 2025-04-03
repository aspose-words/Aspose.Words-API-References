---
title: RelativeHorizontalPosition enumeration
linktitle: RelativeHorizontalPosition enumeration
articleTitle: RelativeHorizontalPosition enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.RelativeHorizontalPosition enumeration. Specifies to what the horizontal position of a shape or text frame is relative."
type: docs
weight: 310
url: /nodejs-net/aspose.words.drawing/relativehorizontalposition/
---

## RelativeHorizontalPosition enumeration

Specifies to what the horizontal position of a shape or text frame is relative.


### Members

| Name | Description |
| --- | --- |
| Margin | Specifies that the horizontal positioning shall be relative to the page margins. |
| Page | The object is positioned relative to the left edge of the page. |
| Column | The object is positioned relative to the left side of the column. |
| Character | The object is positioned relative to the left side of the paragraph. |
| LeftMargin | Specifies that the horizontal positioning shall be relative to the left margin of the page. |
| RightMargin | Specifies that the horizontal positioning shall be relative to the right margin of the page. |
| InsideMargin | Specifies that the horizontal positioning shall be relative to the inside margin of the  current page (the left margin on odd pages, right on even pages). |
| OutsideMargin | Specifies that the horizontal positioning shall be relative to the outside margin of the  current page (the right margin on odd pages, left on even pages). |
| Default | Default value is [RelativeHorizontalPosition.Column](./#Column). |

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
* property [ShapeBase.relativeHorizontalPosition](../shapebase/relativeHorizontalPosition/)

