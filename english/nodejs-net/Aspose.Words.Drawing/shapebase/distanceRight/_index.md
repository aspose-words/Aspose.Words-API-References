---
title: ShapeBase.distanceRight property
linktitle: distanceRight property
articleTitle: distanceRight property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.distanceRight property. Returns or sets the distance (in points) between the document text and the right edge of the shape."
type: docs
weight: 100
url: /nodejs-net/Aspose.Words.Drawing/shapebase/distanceRight/
---

## ShapeBase.distanceRight property

Returns or sets the distance (in points) between the document text and the right edge of the shape.


```js
get distanceRight(): number
```

### Remarks

The default value is 1/8 inch.

Has effect only for top level shapes.




### Examples

Shows how to set the wrapping distance for a text that surrounds a shape.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a rectangle and, get the text to wrap tightly around its bounds.
let shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, 150, 150);
shape.wrapType = aw.Drawing.WrapType.Tight;

// Set the minimum distance between the shape and surrounding text to 40pt from all sides.
shape.distanceTop = 40;
shape.distanceBottom = 40;
shape.distanceLeft = 40;
shape.distanceRight = 40;

// Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
shape.top = 75;
shape.left = 150;
shape.rotation = 60;

// Add text that will wrap around the shape.
builder.font.size = 24;
builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
      "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.save(base.artifactsDir + "Shape.Coordinates.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

