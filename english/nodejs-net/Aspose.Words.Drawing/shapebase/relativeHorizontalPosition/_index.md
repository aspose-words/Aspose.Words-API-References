---
title: ShapeBase.relativeHorizontalPosition property
linktitle: relativeHorizontalPosition property
articleTitle: relativeHorizontalPosition property
second_title: Aspose.Words for Node.js
description: "ShapeBase.relativeHorizontalPosition property. Specifies relative to what the shape is positioned horizontally."
type: docs
weight: 400
url: /nodejs-net/aspose.words.drawing/shapebase/relativeHorizontalPosition/
---

## ShapeBase.relativeHorizontalPosition property

Specifies relative to what the shape is positioned horizontally.


```js
get relativeHorizontalPosition(): Aspose.Words.Drawing.RelativeHorizontalPosition
```

### Remarks

The default value is [RelativeHorizontalPosition.Column](../../relativehorizontalposition/#Column).

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

