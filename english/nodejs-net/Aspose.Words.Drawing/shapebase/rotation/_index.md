---
title: ShapeBase.rotation property
linktitle: rotation property
articleTitle: rotation property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.rotation property. Defines the angle (in degrees) that a shape is rotated"
type: docs
weight: 450
url: /nodejs-net/aspose.words.drawing/shapebase/rotation/
---

## ShapeBase.rotation property

Defines the angle (in degrees) that a shape is rotated.
Positive value corresponds to clockwise rotation angle.


```js
get rotation(): number
```

### Remarks

The default value is 0.




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

