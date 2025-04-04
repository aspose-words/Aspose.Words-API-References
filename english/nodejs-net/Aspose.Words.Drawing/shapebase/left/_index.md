---
title: ShapeBase.left property
linktitle: left property
articleTitle: left property
second_title: Aspose.Words for Node.js
description: "ShapeBase.left property. Gets or sets the position of the left edge of the containing block of the shape."
type: docs
weight: 340
url: /nodejs-net/aspose.words.drawing/shapebase/left/
---

## ShapeBase.left property

Gets or sets the position of the left edge of the containing block of the shape.


```js
get left(): number
```

### Remarks

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.




### Examples

Shows how to insert a floating image, and specify its position and size.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertImage(base.imageDir + "Logo.jpg");
shape.wrapType = aw.Drawing.WrapType.None;

// Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
// as the shape's horizontal distance, in points, from the left side of the page. 
shape.relativeHorizontalPosition = aw.Drawing.RelativeHorizontalPosition.Page;

// Set the shape's horizontal distance from the left side of the page to 100.
shape.left = 100;

// Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
shape.relativeVerticalPosition = aw.Drawing.RelativeVerticalPosition.Page;
shape.top = 80;

// Set the shape's height, which will automatically scale the width to preserve dimensions.
shape.height = 125;

expect(shape.width).toEqual(125.0);

// The "Bottom" and "Right" properties contain the bottom and right edges of the image.
expect(shape.bottom).toEqual(shape.top + shape.height);
expect(shape.right).toEqual(shape.left + shape.width);

doc.save(base.artifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

