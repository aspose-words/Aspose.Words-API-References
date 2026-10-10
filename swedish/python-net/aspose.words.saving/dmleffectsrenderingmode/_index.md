---
title: DmlEffectsRenderingMode enumeration
linktitle: DmlEffectsRenderingMode enumeration
articleTitle: DmlEffectsRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.DmlEffectsRenderingMode enumeration. Specifies how DrawingML effects are rendered to fixed page formats."
type: docs
weight: 80
url: /sv/python-net/aspose.words.saving/dmleffectsrenderingmode/
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

* module [aspose.words.saving](../)

