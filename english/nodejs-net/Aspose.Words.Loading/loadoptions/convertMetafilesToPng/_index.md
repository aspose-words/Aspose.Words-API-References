---
title: LoadOptions.convertMetafilesToPng property
linktitle: convertMetafilesToPng property
articleTitle: convertMetafilesToPng property
second_title: Aspose.Words for Node.js
description: "LoadOptions.convertMetafilesToPng property. Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format."
type: docs
weight: 30
url: /nodejs-net/aspose.words.loading/loadoptions/convertMetafilesToPng/
---

## LoadOptions.convertMetafilesToPng property

Gets or sets whether to convert metafile(Wmf or Emf)
images to Png image format.



```js
get convertMetafilesToPng(): boolean
```

### Remarks

Metafiles (Wmf or Emf)
is an uncompressed image format and sometimes requires to much RAM to hold and process document.
This option allows to convert all metafile images to Png on document loading.
Please note - conversion vector graphics to raster decreases quality of the images.



### Examples

Shows how to convert WMF/EMF to PNG during loading document.

```js
let doc = new aw.Document();

let shape = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Image);
shape.imageData.setImage(base.imageDir + "Windows MetaFile.wmf");
shape.width = 100;
shape.height = 100;

doc.firstSection.body.firstParagraph.appendChild(shape);

doc.save(base.artifactsDir + "Image.CreateImageDirectly.docx");

shape = doc.getShape(0, true);

TestUtil.verifyImageInShape(1600, 1600, aw.Drawing.ImageType.Wmf, shape);

let loadOptions = new aw.Loading.LoadOptions();
loadOptions.convertMetafilesToPng = true;

doc = new aw.Document(base.artifactsDir + "Image.CreateImageDirectly.docx", loadOptions);
shape = doc.getShape(0, true);

TestUtil.verifyImageInShape(1666, 1666, aw.Drawing.ImageType.Png, shape);
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

