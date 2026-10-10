---
title: PdfSaveOptions.zoom_factor property
linktitle: zoom_factor property
articleTitle: zoom_factor property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.zoom_factor property. Gets or sets a value determining zoom factor (in percentages) for a document."
type: docs
weight: 380
url: /es/python-net/aspose.words.saving/pdfsaveoptions/zoom_factor/
---

## PdfSaveOptions.zoom_factor property

Gets or sets a value determining zoom factor (in percentages) for a document.


```python
@property
def zoom_factor(self) -> int:
    ...

@zoom_factor.setter
def zoom_factor(self, value: int):
    ...

```

### Remarks

This value is used only if [PdfSaveOptions.zoom_behavior](../zoom_behavior/) is set to [PdfZoomBehavior.ZOOM_FACTOR](../../pdfzoombehavior/#ZOOM_FACTOR).



### Examples

Shows how to set the default zooming that a reader applies when opening a rendered PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
# Establezca la propiedad "ZoomBehavior" a "PdfZoomBehavior.ZoomFactor" para que un lector de PDF
# aplique un factor de zoom basado en porcentaje cuando abramos el documento con él.
# Establezca la propiedad "ZoomFactor" a "25" para dar al factor de zoom un valor del 25%.
options = aw.saving.PdfSaveOptions()
options.zoom_behavior = aw.saving.PdfZoomBehavior.ZOOM_FACTOR
options.zoom_factor = 25
# Al abrir este documento con un lector como Adobe Acrobat, veremos el documento escalado a 1/4 de su tamaño real.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ZoomBehaviour.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

