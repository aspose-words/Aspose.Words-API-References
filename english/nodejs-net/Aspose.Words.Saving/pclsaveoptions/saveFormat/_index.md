---
title: PclSaveOptions.saveFormat property
linktitle: saveFormat property
articleTitle: saveFormat property
second_title: Aspose.Words for NodeJs
description: "PclSaveOptions.saveFormat property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/pclsaveoptions/saveFormat/
---

## PclSaveOptions.saveFormat property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.Pcl](../../../aspose.words/saveformat/#Pcl).



```js
get saveFormat(): Aspose.Words.SaveFormat
```

### Examples

Shows how to rasterize complex elements while saving a document to PCL.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let saveOptions = new aw.Saving.PclSaveOptions();
saveOptions.saveFormat = aw.SaveFormat.Pcl;
saveOptions.rasterizeTransformedElements = true

doc.save(base.artifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PclSaveOptions](../)

