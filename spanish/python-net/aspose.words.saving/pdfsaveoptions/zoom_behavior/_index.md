---
title: PdfSaveOptions.zoom_behavior property
linktitle: zoom_behavior property
articleTitle: zoom_behavior property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.zoom_behavior property. Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer."
type: docs
weight: 370
url: /es/python-net/aspose.words.saving/pdfsaveoptions/zoom_behavior/
---

## PdfSaveOptions.zoom_behavior property

Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer.


```python
@property
def zoom_behavior(self) -> aspose.words.saving.PdfZoomBehavior:
    ...

@zoom_behavior.setter
def zoom_behavior(self, value: aspose.words.saving.PdfZoomBehavior):
    ...

```

### Remarks

The default value is [PdfZoomBehavior.NONE](../../pdfzoombehavior/#NONE), i.e. no fit is applied.



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

