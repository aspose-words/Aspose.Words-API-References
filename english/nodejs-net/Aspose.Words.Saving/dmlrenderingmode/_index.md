---
title: DmlRenderingMode enumeration
linktitle: DmlRenderingMode enumeration
articleTitle: DmlRenderingMode enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.DmlRenderingMode enumeration. Specifies how DrawingML shapes are rendered to fixed page formats."
type: docs
weight: 90
url: /nodejs-net/aspose.words.saving/dmlrenderingmode/
---

## DmlRenderingMode enumeration

Specifies how DrawingML shapes are rendered to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| Fallback | If fall-back shape is available for DrawingML, Aspose.Words renders fall-back shape instead of the DrawingML. |
| DrawingML | Aspose.Words ignores fall-back shape of DrawingML and renders DrawingML itself. This is the default mode. |

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

* module [Aspose.Words.Saving](../)

