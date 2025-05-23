﻿---
title: SaveOptions.dml_effects_rendering_mode property
linktitle: dml_effects_rendering_mode property
articleTitle: dml_effects_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.dml_effects_rendering_mode property. Gets or sets a value determining how DrawingML effects are rendered."
type: docs
weight: 40
url: /python-net/aspose.words.saving/saveoptions/dml_effects_rendering_mode/
---

## SaveOptions.dml_effects_rendering_mode property

Gets or sets a value determining how DrawingML effects are rendered.


```python
@property
def dml_effects_rendering_mode(self) -> aspose.words.saving.DmlEffectsRenderingMode:
    ...

@dml_effects_rendering_mode.setter
def dml_effects_rendering_mode(self, value: aspose.words.saving.DmlEffectsRenderingMode):
    ...

```

### Remarks

The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../dmleffectsrenderingmode/#SIMPLIFIED).
This property is used when the document is exported to fixed page formats.




### Examples

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape effects.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
# Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
# to render a simplified version of DrawingML effects.
# Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
# render DrawingML effects with more accuracy and also with more processing cost.
options.dml_effects_rendering_mode = effects_rendering_mode
self.assertEqual(aw.saving.DmlRenderingMode.DRAWING_ML, options.dml_rendering_mode)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLEffects.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

