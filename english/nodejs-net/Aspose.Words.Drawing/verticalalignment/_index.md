---
title: VerticalAlignment enumeration
linktitle: VerticalAlignment enumeration
articleTitle: VerticalAlignment enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.VerticalAlignment enumeration. Specifies vertical alignment of a floating shape, text frame or a floating table."
type: docs
weight: 520
url: /nodejs-net/Aspose.Words.Drawing/verticalalignment/
---

## VerticalAlignment enumeration

Specifies vertical alignment of a floating shape, text frame or a floating table.


### Members

| Name | Description |
| --- | --- |
| None | The object is explicitly positioned, usually using its **Top** property. |
| Top | Specifies that the object shall be at the top of the vertical alignment base. |
| Center | Specifies that the object shall be centered with respect to the vertical alignment base. |
| Bottom | Specifies that the object shall be at the bottom of the vertical alignment base. |
| Inside | Specifies that the object shall be inside of the horizontal alignment base. |
| Outside | Specifies that the object shall be outside of the vertical alignment base. |
| Inline | Not documented. Seems to be a possible value for floating paragraphs and tables. |
| Default | Same as [VerticalAlignment.None](./#None). |

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
* property [ShapeBase.verticalAlignment](../shapebase/verticalAlignment/)

