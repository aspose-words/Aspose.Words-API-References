---
title: ShapeBase.behindText property
linktitle: behindText property
articleTitle: behindText property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.behindText property. Specifies whether the shape is below or above text."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Drawing/shapebase/behindText/
---

## ShapeBase.behindText property

Specifies whether the shape is below or above text.


```js
get behindText(): boolean
```

### Remarks

Has effect only for top level shapes.

The default value is ``false``.




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
* property [ShapeBase.zorder](../zorder/)

