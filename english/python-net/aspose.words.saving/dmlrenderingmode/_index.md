---
title: DmlRenderingMode enumeration
linktitle: DmlRenderingMode enumeration
articleTitle: DmlRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.DmlRenderingMode enumeration. Specifies how DrawingML shapes are rendered to fixed page formats."
type: docs
weight: 90
url: /python-net/aspose.words.saving/dmlrenderingmode/
---

## DmlRenderingMode enumeration

Specifies how DrawingML shapes are rendered to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| FALLBACK | If fall-back shape is available for DrawingML, Aspose.Words renders fall-back shape instead of the DrawingML. |
| DRAWING_ML | Aspose.Words ignores fall-back shape of DrawingML and renders DrawingML itself. This is the default mode. |

### Examples

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```python
doc = aw.Document(MY_DIR + 'DrawingML shape effects.docx')
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
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.drawing_ml_effects.pdf', options)
```

Shows how to render fallback shapes when saving to PDF.

```python
doc = aw.Document(MY_DIR + 'DrawingML shape fallbacks.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Set the "dml_rendering_mode" property to "DmlRenderingMode.FALLBACK"
# to substitute DML shapes with their fallback shapes.
# Set the "dml_rendering_mode" property to "DmlRenderingMode.DRAWING_ML"
# to render the DML shapes themselves.
options.dml_rendering_mode = dml_rendering_mode
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.drawing_ml_fallback.pdf', options)
```

### See Also

* module [aspose.words.saving](../)

