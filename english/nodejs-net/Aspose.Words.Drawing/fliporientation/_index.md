---
title: FlipOrientation enumeration
linktitle: FlipOrientation enumeration
articleTitle: FlipOrientation enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.FlipOrientation enumeration. Possible values for the orientation of a shape."
type: docs
weight: 110
url: /nodejs-net/Aspose.Words.Drawing/fliporientation/
---

## FlipOrientation enumeration

Possible values for the orientation of a shape.


### Members

| Name | Description |
| --- | --- |
| None | Coordinates are not flipped. |
| Horizontal | Flip along the y-axis, reversing the x-coordinates. |
| Vertical | Flip along the x-axis, reversing the y-coordinates. |
| Both | Flip along both the y- and x-axis. |

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

* module [Aspose.Words.Drawing](../)
* property [ShapeBase.flipOrientation](../shapebase/flipOrientation/)

