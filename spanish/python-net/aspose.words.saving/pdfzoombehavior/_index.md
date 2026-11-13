---
title: PdfZoomBehavior enumeration
linktitle: PdfZoomBehavior enumeration
articleTitle: PdfZoomBehavior enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfZoomBehavior enumeration. Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer."
type: docs
weight: 770
url: /es/python-net/aspose.words.saving/pdfzoombehavior/
---

## PdfZoomBehavior enumeration

Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer.


### Members

| Name | Description |
| --- | --- |
| NONE | How the document is displayed is left to the PDF viewer. Usually the viewer displays the document to fit page width. |
| ZOOM_FACTOR | Displays the page using the specified zoom factor. |
| FIT_PAGE | Displays the page so it visible entirely. |
| FIT_WIDTH | Fits the width of the page. |
| FIT_HEIGHT | Fits the height of the page. |
| FIT_BOX | Fits the bounding box (rectangle containing all visible elements on the page). |

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

* module [aspose.words.saving](../)

