---
title: LoadOptions.baseUri property
linktitle: baseUri property
articleTitle: baseUri property
second_title: Aspose.Words for NodeJs
description: "LoadOptions.baseUri property. Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Loading/loadoptions/baseUri/
---

## LoadOptions.baseUri property

Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required.
Can be ``null`` or empty string. Default is ``null``.



```js
get baseUri(): string
```

### Remarks

This property is used to resolve relative URIs into absolute in the following cases:


1. When loading an HTML document from a stream and the document contains images with
   relative URIs and does not have a base URI specified in the BASE HTML element.
   
1. When saving a document to PDF and other formats, to retrieve images linked using relative URIs
   so the images can be saved into the output document.
   



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

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

