---
title: FixedPageSaveOptions.color_mode property
linktitle: color_mode property
articleTitle: color_mode property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.color_mode property. Gets or sets a value determining how colors are rendered."
type: docs
weight: 10
url: /es/python-net/aspose.words.saving/fixedpagesaveoptions/color_mode/
---

## FixedPageSaveOptions.color_mode property

Gets or sets a value determining how colors are rendered.


```python
@property
def color_mode(self) -> aspose.words.saving.ColorMode:
    ...

@color_mode.setter
def color_mode(self, value: aspose.words.saving.ColorMode):
    ...

```

### Remarks

The default value is [ColorMode.NORMAL](../../colormode/#NORMAL).



### Examples

Shows how to change image color with saving options property.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
# Establezca la propiedad "ColorMode" en "Grayscale" para renderizar todas las imágenes del documento en blanco y negro.
# El tamaño del documento de salida puede ser mayor con esta configuración.
# Establezca la propiedad "ColorMode" en "Normal" para renderizar todas las imágenes en color.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.color_mode = color_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ColorRendering.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

