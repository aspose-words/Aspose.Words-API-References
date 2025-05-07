---
title: ShapeBase.isImage property
linktitle: isImage property
articleTitle: isImage property
second_title: Aspose.Words for Node.js
description: "ShapeBase.isImage property. Returns ``true`` if this shape is an image shape."
type: docs
weight: 300
url: /nodejs-net/aspose.words.drawing/shapebase/isImage/
---

## ShapeBase.isImage property

Returns ``true`` if this shape is an image shape.



```js
get isImage(): boolean
```

### Examples

Shows how to open an HTML document with images from a stream using a base URI.

```js
const buffer = base.loadFileToBuffer(base.myDir + "Document.html");
// Pass the URI of the base folder while loading it
// so that any images with relative URIs in the HTML document can be found.
const loadOptions = new aw.Loading.LoadOptions();
loadOptions.baseUri = base.imageDir;
const doc = new aw.Document(buffer, loadOptions);
// Verify that the first shape of the document contains a valid image.
const shape = doc.getShape(0, true);
expect(shape.isImage).toEqual(true);
expect(shape.imageData.imageBytes).not.toEqual(null);
expect(aw.ConvertUtil.pointToPixel(shape.width)).toBeCloseTo(32, 2);
expect(aw.ConvertUtil.pointToPixel(shape.height)).toBeCloseTo(32, 2);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

