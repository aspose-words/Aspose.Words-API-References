---
title: PclSaveOptions.rasterizeTransformedElements property
linktitle: rasterizeTransformedElements property
articleTitle: rasterizeTransformedElements property
second_title: Aspose.Words for NodeJs
description: "PclSaveOptions.rasterizeTransformedElements property. Gets or sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/pclsaveoptions/rasterizeTransformedElements/
---

## PclSaveOptions.rasterizeTransformedElements property

Gets or sets a value determining whether or not complex transformed elements
should be rasterized before saving to PCL document.
Default is ``True``.



```js
get rasterizeTransformedElements(): boolean
```

### Remarks

PCL doesn't support some kind of transformations that are used by Aspose Words.
E.g. rotated, skewed images and texture brushes. To properly render such elements
rasterization process is used, i.e. saving to image and clipping.
This process can take additional time and memory.
If flag is set to ``False``, some content in output may be different
as compared with the source document.



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

