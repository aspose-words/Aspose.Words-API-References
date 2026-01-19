---
title: ImlRenderingMode enumeration
linktitle: ImlRenderingMode enumeration
articleTitle: ImlRenderingMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.ImlRenderingMode enumeration. Specifies how ink (InkML) objects are rendered to fixed page formats."
type: docs
weight: 400
url: /nodejs-net/aspose.words.saving/imlrenderingmode/
---

## ImlRenderingMode enumeration

Specifies how ink (InkML) objects are rendered to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| Fallback | If fall-back shape is available for ink (InkML) object, Aspose.Words renders fall-back shape instead of the InkML. |
| InkML | Aspose.Words ignores fall-back shape of ink (InkML) object and renders InkML itself. This is the default mode. |

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

* module [Aspose.Words.Saving](../)

