---
title: ShapeBase.canHaveImage property
linktitle: canHaveImage property
articleTitle: canHaveImage property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.canHaveImage property. Returns ``True`` if the shape type allows the shape to have an image."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Drawing/shapebase/canHaveImage/
---

## ShapeBase.canHaveImage property

Returns ``True`` if the shape type allows the shape to have an image.



```js
get canHaveImage(): boolean
```

### Remarks

Although Microsoft Word has a special shape type for images, it appears that in Microsoft Word documents any shape
except a group shape can have an image, therefore this property returns ``True`` for all shapes except [GroupShape](../../groupshape/).




### Examples

Shows how to insert and rotate an image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a shape with an image.
let shape = builder.insertImage(base.imageDir + "Logo.jpg");
expect(shape.canHaveImage).toEqual(true);
expect(shape.hasImage).toEqual(true);

// Rotate the image 45 degrees clockwise.
shape.rotation = 45;

doc.save(base.artifactsDir + "Shape.Rotate.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

