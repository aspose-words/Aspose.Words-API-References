---
title: SaveOptions.dml_rendering_mode property
linktitle: dml_rendering_mode property
articleTitle: dml_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.dml_rendering_mode property. Gets or sets a value determining how DrawingML shapes are rendered."
type: docs
weight: 50
url: /fr/python-net/aspose.words.saving/saveoptions/dml_rendering_mode/
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
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
options = aw.saving.PdfSaveOptions()
# Définissez la propriété "DmlEffectsRenderingMode" sur "DmlEffectsRenderingMode.None" pour ignorer tous les effets DrawingML.
# Définissez la propriété "DmlEffectsRenderingMode" sur "DmlEffectsRenderingMode.Simplified"
# pour rendre une version simplifiée des effets DrawingML.
# Définissez la propriété "DmlEffectsRenderingMode" sur "DmlEffectsRenderingMode.Fine" pour
# rendre les effets DrawingML avec plus de précision, mais aussi avec un coût de traitement plus élevé.
options.dml_effects_rendering_mode = effects_rendering_mode
self.assertEqual(aw.saving.DmlRenderingMode.DRAWING_ML, options.dml_rendering_mode)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLEffects.pdf', save_options=options)
```

Shows how to render fallback shapes when saving to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape fallbacks.docx')
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
options = aw.saving.PdfSaveOptions()
# Définissez la propriété "DmlRenderingMode" sur "DmlRenderingMode.Fallback"
# pour remplacer les formes DML par leurs formes de secours.
# Définissez la propriété "DmlRenderingMode" sur "DmlRenderingMode.DrawingML"
# pour rendre les formes DML elles‑mêmes.
options.dml_rendering_mode = dml_rendering_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLFallback.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

