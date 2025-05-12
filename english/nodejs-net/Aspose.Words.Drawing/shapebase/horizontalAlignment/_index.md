---
title: ShapeBase.horizontalAlignment property
linktitle: horizontalAlignment property
articleTitle: horizontalAlignment property
second_title: Aspose.Words for Node.js
description: "ShapeBase.horizontalAlignment property. Specifies how the shape is positioned horizontally."
type: docs
weight: 240
url: /nodejs-net/aspose.words.drawing/shapebase/horizontalAlignment/
---

## ShapeBase.horizontalAlignment property

Specifies how the shape is positioned horizontally.


```js
get horizontalAlignment(): Aspose.Words.Drawing.HorizontalAlignment
```

### Remarks

The default value is [HorizontalAlignment.None](../../horizontalalignment/#None).

Has effect only for top level floating shapes.




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

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

