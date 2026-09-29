---
title: SaveOptions.dml_rendering_mode property
linktitle: dml_rendering_mode property
articleTitle: dml_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.dml_rendering_mode property. Gets or sets a value determining how DrawingML shapes are rendered."
type: docs
weight: 50
url: /es/python-net/aspose.words.saving/saveoptions/dml_rendering_mode/
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
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "DmlEffectsRenderingMode" a "DmlEffectsRenderingMode.None" para descartar todos los efectos DrawingML.
# Establezca la propiedad "DmlEffectsRenderingMode" a "DmlEffectsRenderingMode.Simplified"
# para renderizar una versión simplificada de los efectos DrawingML.
# Establezca la propiedad "DmlEffectsRenderingMode" a "DmlEffectsRenderingMode.Fine" para
# renderizar los efectos DrawingML con mayor precisión y también con mayor costo de procesamiento.
options.dml_effects_rendering_mode = effects_rendering_mode
self.assertEqual(aw.saving.DmlRenderingMode.DRAWING_ML, options.dml_rendering_mode)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLEffects.pdf', save_options=options)
```

Shows how to render fallback shapes when saving to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape fallbacks.docx')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "DmlRenderingMode" a "DmlRenderingMode.Fallback"
# para sustituir las formas DML por sus formas de reserva.
# Establezca la propiedad "DmlRenderingMode" a "DmlRenderingMode.DrawingML"
# para renderizar las propias formas DML.
options.dml_rendering_mode = dml_rendering_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLFallback.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

