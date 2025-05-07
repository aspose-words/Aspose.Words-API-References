---
title: ImageSize.widthPoints property
linktitle: widthPoints property
articleTitle: widthPoints property
second_title: Aspose.Words for Node.js
description: "ImageSize.widthPoints property. Gets the width of the image in points"
type: docs
weight: 70
url: /nodejs-net/aspose.words.drawing/imagesize/widthPoints/
---

## ImageSize.widthPoints property

Gets the width of the image in points. 1 point is 1/72 inch.


```js
get widthPoints(): number
```

### Examples

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
* class [ImageSize](../)

