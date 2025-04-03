---
title: SaveOptions.dmlEffectsRenderingMode property
linktitle: dmlEffectsRenderingMode property
articleTitle: dmlEffectsRenderingMode property
second_title: Aspose.Words for NodeJs
description: "SaveOptions.dmlEffectsRenderingMode property. Gets or sets a value determining how DrawingML effects are rendered."
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/saveoptions/dmlEffectsRenderingMode/
---

## SaveOptions.dmlEffectsRenderingMode property

Gets or sets a value determining how DrawingML effects are rendered.


```js
get dmlEffectsRenderingMode(): Aspose.Words.Saving.DmlEffectsRenderingMode
```

### Remarks

The default value is [DmlEffectsRenderingMode.Simplified](../../dmleffectsrenderingmode/#Simplified).
This property is used when the document is exported to fixed page formats.




### Examples

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```js
let doc = new aw.Document(base.myDir + "DrawingML shape effects.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
// Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
// to render a simplified version of DrawingML effects.
// Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
// render DrawingML effects with more accuracy and also with more processing cost.
options.dmlEffectsRenderingMode = effectsRenderingMode;

expect(options.dmlRenderingMode).toEqual(aw.Saving.DmlRenderingMode.DrawingML);

doc.save(base.artifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

