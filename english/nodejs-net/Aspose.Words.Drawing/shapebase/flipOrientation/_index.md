---
title: ShapeBase.flipOrientation property
linktitle: flipOrientation property
articleTitle: flipOrientation property
second_title: Aspose.Words for Node.js
description: "ShapeBase.flipOrientation property. Switches the orientation of a shape."
type: docs
weight: 180
url: /nodejs-net/aspose.words.drawing/shapebase/flipOrientation/
---

## ShapeBase.flipOrientation property

Switches the orientation of a shape.


```js
get flipOrientation(): Aspose.Words.Drawing.FlipOrientation
```

### Remarks

The default value is [FlipOrientation.None](../../fliporientation/#None).




### Examples

Shows how to flip a shape on an axis.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert an image shape and leave its orientation in its default state.
let shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, aw.Drawing.RelativeHorizontalPosition.LeftMargin, 100,
  aw.Drawing.RelativeVerticalPosition.TopMargin, 100, 100, 100, aw.Drawing.WrapType.None);
shape.imageData.setImage(base.imageDir + "Logo.jpg");

expect(shape.flipOrientation).toEqual(aw.Drawing.FlipOrientation.None);

shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, aw.Drawing.RelativeHorizontalPosition.LeftMargin, 250,
  aw.Drawing.RelativeVerticalPosition.TopMargin, 100, 100, 100, aw.Drawing.WrapType.None);
shape.imageData.setImage(base.imageDir + "Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the second shape on the y-axis,
// making it into a horizontal mirror image of the first shape.
shape.flipOrientation = aw.Drawing.FlipOrientation.Horizontal;

shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, aw.Drawing.RelativeHorizontalPosition.LeftMargin, 100,
  aw.Drawing.RelativeVerticalPosition.TopMargin, 250, 100, 100, aw.Drawing.WrapType.None);
shape.imageData.setImage(base.imageDir + "Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the third shape on the x-axis,
// making it into a vertical mirror image of the first shape.
shape.flipOrientation = aw.Drawing.FlipOrientation.Vertical;

shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, aw.Drawing.RelativeHorizontalPosition.LeftMargin, 250,
  aw.Drawing.RelativeVerticalPosition.TopMargin, 250, 100, 100, aw.Drawing.WrapType.None);
shape.imageData.setImage(base.imageDir + "Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the fourth shape on both the x and y axes,
// making it into a horizontal and vertical mirror image of the first shape.
shape.flipOrientation = aw.Drawing.FlipOrientation.Both;

doc.save(base.artifactsDir + "Shape.FlipShapeOrientation.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

