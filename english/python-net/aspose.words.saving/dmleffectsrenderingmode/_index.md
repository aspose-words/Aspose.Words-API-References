---
title: DmlEffectsRenderingMode enumeration
linktitle: DmlEffectsRenderingMode enumeration
articleTitle: DmlEffectsRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.DmlEffectsRenderingMode enumeration. Specifies how DrawingML effects are rendered to fixed page formats."
type: docs
weight: 70
url: /python-net/aspose.words.saving/dmleffectsrenderingmode/
---

## DmlEffectsRenderingMode enumeration

Specifies how DrawingML effects are rendered to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| SIMPLIFIED | Rendering of DrawingML effects are simplified. |
| NONE | No DrawingML effects are rendered. |
| FINE | DrawingML effects are rendered in fine mode which involves advanced processing. In this mode rendering of effects gives better results but at a higher performance cost than [DmlEffectsRenderingMode.SIMPLIFIED](./#SIMPLIFIED) mode. |

### Examples

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```python
doc = aw.Document(MY_DIR + "DrawingML shape effects.docx")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Set the "dml_effects_rendering_mode" property to "DmlEffectsRenderingMode.NONE" to discard all DrawingML effects.
# Set the "dml_effects_rendering_mode" property to "DmlEffectsRenderingMode.SIMPLIFIED"
# to render a simplified version of DrawingML effects.
# Set the "dml_effects_rendering_mode" property to "DmlEffectsRenderingMode.FINE" to
# render DrawingML effects with more accuracy and also with more processing cost.
options.dml_effects_rendering_mode = effects_rendering_mode

self.assertEqual(aw.saving.DmlRenderingMode.DRAWING_ML, options.dml_rendering_mode)

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.drawing_ml_effects.pdf", options)
```

### See Also

* module [aspose.words.saving](../)

