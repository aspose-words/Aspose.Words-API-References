---
title: SaveOptions.dml_rendering_mode property
linktitle: dml_rendering_mode property
articleTitle: dml_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.dml_rendering_mode property. Gets or sets a value determining how DrawingML shapes are rendered."
type: docs
weight: 50
url: /de/python-net/aspose.words.saving/saveoptions/dml_rendering_mode/
---

## SaveOptions.dml_rendering_mode property

Gets or sets a value determining how DrawingML shapes are rendered.


```python
@property
def dml_rendering_mode(self) -> aspose.words.saving.DmlRenderingMode:
    ...

@dml_rendering_mode.setter
def dml_rendering_mode(self, value: aspose.words.saving.DmlRenderingMode):
    ...

```

### Remarks

The default value is [DmlRenderingMode.FALLBACK](../../dmlrenderingmode/#FALLBACK).
This property is used when the document is exported to fixed page formats.




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

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

