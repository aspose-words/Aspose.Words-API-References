---
title: DmlRenderingMode enumeration
linktitle: DmlRenderingMode enumeration
articleTitle: DmlRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.DmlRenderingMode enumeration. Specifies how DrawingML shapes are rendered to fixed page formats."
type: docs
weight: 90
url: /de/python-net/aspose.words.saving/dmlrenderingmode/
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
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape effects.docx')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Setzen Sie die "DmlEffectsRenderingMode"-Eigenschaft auf "DmlEffectsRenderingMode.None", um alle DrawingML-Effekte zu verwerfen.
# Setzen Sie die "DmlEffectsRenderingMode"-Eigenschaft auf "DmlEffectsRenderingMode.Simplified"
# um eine vereinfachte Version der DrawingML-Effekte zu rendern.
# Setzen Sie die "DmlEffectsRenderingMode"-Eigenschaft auf "DmlEffectsRenderingMode.Fine", um
# DrawingML-Effekte mit höherer Genauigkeit und zudem mit höherem Verarbeitungsaufwand zu rendern.
options.dml_effects_rendering_mode = effects_rendering_mode
self.assertEqual(aw.saving.DmlRenderingMode.DRAWING_ML, options.dml_rendering_mode)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLEffects.pdf', save_options=options)
```

Shows how to render fallback shapes when saving to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape fallbacks.docx')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Setzen Sie die "DmlRenderingMode"-Eigenschaft auf "DmlRenderingMode.Fallback"
# um DML-Formen durch ihre Ersatzformen zu ersetzen.
# Setzen Sie die "DmlRenderingMode"-Eigenschaft auf "DmlRenderingMode.DrawingML"
# um die DML-Formen selbst zu rendern.
options.dml_rendering_mode = dml_rendering_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLFallback.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

