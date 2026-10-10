---
title: PdfZoomBehavior enumeration
linktitle: PdfZoomBehavior enumeration
articleTitle: PdfZoomBehavior enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfZoomBehavior enumeration. Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer."
type: docs
weight: 770
url: /de/python-net/aspose.words.saving/pdfzoombehavior/
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
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
# Setzen Sie die Eigenschaft "ZoomBehavior" auf "PdfZoomBehavior.ZoomFactor", um einen PDF‑Reader zu
# veranlassen, einen prozentbasierten Zoom‑Faktor anzuwenden, wenn wir das Dokument damit öffnen.
# Setzen Sie die Eigenschaft "ZoomFactor" auf "25", um dem Zoom‑Faktor den Wert 25 % zu geben.
options = aw.saving.PdfSaveOptions()
options.zoom_behavior = aw.saving.PdfZoomBehavior.ZOOM_FACTOR
options.zoom_factor = 25
# Wenn wir dieses Dokument mit einem Reader wie Adobe Acrobat öffnen, sehen wir das Dokument auf ein Viertel seiner tatsächlichen Größe skaliert.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ZoomBehaviour.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

