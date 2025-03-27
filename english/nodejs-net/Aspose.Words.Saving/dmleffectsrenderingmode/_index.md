---
title: DmlEffectsRenderingMode enumeration
linktitle: DmlEffectsRenderingMode enumeration
articleTitle: DmlEffectsRenderingMode enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.DmlEffectsRenderingMode enumeration. Specifies how DrawingML effects are rendered to fixed page formats."
type: docs
weight: 80
url: /nodejs-net/Aspose.Words.Saving/dmleffectsrenderingmode/
---

## DmlEffectsRenderingMode enumeration

Specifies how DrawingML effects are rendered to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| Simplified | Rendering of DrawingML effects are simplified. |
| None | No DrawingML effects are rendered. |
| Fine | DrawingML effects are rendered in fine mode which involves advanced processing. In this mode rendering of effects gives better results but at a higher performance cost than [DmlEffectsRenderingMode.Simplified](./#Simplified) mode. |

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

* module [Aspose.Words.Saving](../)

