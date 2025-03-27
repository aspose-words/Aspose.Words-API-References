---
title: ShapeBase.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.width property. Gets or sets the width of the containing block of the shape."
type: docs
weight: 550
url: /nodejs-net/Aspose.Words.Drawing/shapebase/width/
---

## ShapeBase.width property

Gets or sets the width of the containing block of the shape.


```js
get width(): number
```

### Remarks

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.




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

Shows how to resize a shape with an image.

```js
// When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
// when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let shape = builder.insertImage(base.imageDir + "Logo.jpg");

// A 400x400 image will create an ImageData object with an image size of 300x300pt.
let imageSize = shape.imageData.imageSize;

expect(imageSize.widthPoints).toEqual(300.0);
expect(imageSize.heightPoints).toEqual(300.0);

// If a shape's dimensions match the image data's dimensions,
// then the shape is displaying the image in its original size.
expect(shape.width).toEqual(300.0);
expect(shape.height).toEqual(300.0);

// Reduce the overall size of the shape by 50%. 
shape.width *= 0.5;

// Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions. 
expect(shape.width).toEqual(150.0);
expect(shape.height).toEqual(150.0);

// When we resize the shape, the size of the image data remains the same.
expect(imageSize.widthPoints).toEqual(300.0);
expect(imageSize.heightPoints).toEqual(300.0);

// We can reference the image data dimensions to apply a scaling based on the size of the image.
shape.width = imageSize.widthPoints * 1.1;

expect(shape.width).toEqual(330.0);
expect(shape.height).toEqual(330.0);

doc.save(base.artifactsDir + "Image.ScaleImage.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

