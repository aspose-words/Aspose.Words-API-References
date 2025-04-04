---
title: HorizontalAlignment enumeration
linktitle: HorizontalAlignment enumeration
articleTitle: HorizontalAlignment enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.HorizontalAlignment enumeration. Specifies horizontal alignment of a floating shape, text frame or floating table."
type: docs
weight: 180
url: /nodejs-net/aspose.words.drawing/horizontalalignment/
---

## HorizontalAlignment enumeration

Specifies horizontal alignment of a floating shape, text frame or floating table.


### Members

| Name | Description |
| --- | --- |
| None | The object is explicitly positioned, usually using its **Left** property. |
| Default | Same as [HorizontalAlignment.None](./#None). |
| Left | Specifies that the object shall be left aligned to the horizontal alignment base. |
| Center | Specifies that the object shall be centered with respect to the horizontal alignment base. |
| Right | Specifies that the object shall be right aligned to the horizontal alignment base. |
| Inside | Specifies that the object shall be inside of the horizontal alignment base. |
| Outside | Specifies that the object shall be outside of the horizontal alignment base. |

### Examples

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
* property [ShapeBase.horizontalAlignment](../shapebase/horizontalAlignment/)

