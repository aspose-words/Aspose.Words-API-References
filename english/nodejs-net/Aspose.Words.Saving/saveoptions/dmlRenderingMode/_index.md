---
title: SaveOptions.dmlRenderingMode property
linktitle: dmlRenderingMode property
articleTitle: dmlRenderingMode property
second_title: Aspose.Words for Node.js
description: "SaveOptions.dmlRenderingMode property. Gets or sets a value determining how DrawingML shapes are rendered."
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/saveoptions/dmlRenderingMode/
---

## SaveOptions.dmlRenderingMode property

Gets or sets a value determining how DrawingML shapes are rendered.


```js
get dmlRenderingMode(): Aspose.Words.Saving.DmlRenderingMode
```

### Remarks

The default value is [DmlRenderingMode.Fallback](../../dmlrenderingmode/#Fallback).
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

Shows how to render fallback shapes when saving to PDF.

```js
let doc = new aw.Document(base.myDir + "DrawingML shape fallbacks.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "DmlRenderingMode" property to "DmlRenderingMode.Fallback"
// to substitute DML shapes with their fallback shapes.
// Set the "DmlRenderingMode" property to "DmlRenderingMode.DrawingML"
// to render the DML shapes themselves.
options.dmlRenderingMode = dmlRenderingMode;

doc.save(base.artifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

