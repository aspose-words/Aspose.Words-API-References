---
title: SaveOptions.imlRenderingMode property
linktitle: imlRenderingMode property
articleTitle: imlRenderingMode property
second_title: Aspose.Words for Node.js
description: "SaveOptions.imlRenderingMode property. Gets or sets a value determining how ink (InkML) objects are rendered."
type: docs
weight: 70
url: /nodejs-net/aspose.words.saving/saveoptions/imlRenderingMode/
---

## SaveOptions.imlRenderingMode property

Gets or sets a value determining how ink (InkML) objects are rendered.


```js
get imlRenderingMode(): Aspose.Words.Saving.ImlRenderingMode
```

### Remarks

The default value is [ImlRenderingMode.InkML](../../imlrenderingmode/#InkML).
This property is used when the document is exported to fixed page formats.




### Examples

Shows how to render Ink object.

```js
let doc = new aw.Document(base.myDir + "Ink object.docx");

// Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
// If the rendering result is unsatisfactory,
// please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
let saveOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Jpeg)
{
  ImlRenderingMode = aw.Saving.ImlRenderingMode.InkML
};

doc.save(base.artifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

