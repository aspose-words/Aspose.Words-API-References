---
title: SaveOptions.dml_rendering_mode property
linktitle: dml_rendering_mode property
articleTitle: dml_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.dml_rendering_mode property. Gets or sets a value determining how DrawingML shapes are rendered."
type: docs
weight: 50
url: /python-net/aspose.words.saving/saveoptions/dml_rendering_mode/
---

## SaveOptions.dml_rendering_mode property

Gets or sets a value determining how DrawingML shapes are rendered.

The default value is [DmlRenderingMode.FALLBACK](../../dmlrenderingmode/#FALLBACK).
This property is used when the document is exported to fixed page formats.




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

Shows how to render fallback shapes when saving to PDF.

```python
doc = aw.Document(MY_DIR + "DrawingML shape fallbacks.docx")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Set the "dml_rendering_mode" property to "DmlRenderingMode.FALLBACK"
# to substitute DML shapes with their fallback shapes.
# Set the "dml_rendering_mode" property to "DmlRenderingMode.DRAWING_ML"
# to render the DML shapes themselves.
options.dml_rendering_mode = dml_rendering_mode

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.drawing_ml_fallback.pdf", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

