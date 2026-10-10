---
title: PdfSaveOptions.dml_effects_rendering_mode property
linktitle: dml_effects_rendering_mode property
articleTitle: dml_effects_rendering_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.dml_effects_rendering_mode property. Gets or sets a value determining how DrawingML effects are rendered."
type: docs
weight: 100
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/dml_effects_rendering_mode/
---

## PdfSaveOptions.dml_effects_rendering_mode property

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

If [PdfSaveOptions.compliance](../compliance/) is set to [PdfCompliance.PDF_A1A](../../pdfcompliance/#PDF_A1A) or [PdfCompliance.PDF_A1B](../../pdfcompliance/#PDF_A1B),
property always returns [DmlEffectsRenderingMode.NONE](../../dmleffectsrenderingmode/#NONE).




### Examples

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape effects.docx')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "DmlEffectsRenderingMode" till "DmlEffectsRenderingMode.None" för att ta bort alla DrawingML-effekter.
# Ställ in egenskapen "DmlEffectsRenderingMode" till "DmlEffectsRenderingMode.Simplified"
# för att rendera en förenklad version av DrawingML-effekter.
# Ställ in egenskapen "DmlEffectsRenderingMode" till "DmlEffectsRenderingMode.Fine" för att
# rendera DrawingML-effekter med högre noggrannhet men också med högre bearbetningskostnad.
options.dml_effects_rendering_mode = effects_rendering_mode
self.assertEqual(aw.saving.DmlRenderingMode.DRAWING_ML, options.dml_rendering_mode)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLEffects.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

