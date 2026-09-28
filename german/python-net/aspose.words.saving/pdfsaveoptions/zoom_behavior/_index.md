---
title: PdfSaveOptions.zoom_behavior property
linktitle: zoom_behavior property
articleTitle: zoom_behavior property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.zoom_behavior property. Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer."
type: docs
weight: 370
url: /de/python-net/aspose.words.saving/pdfsaveoptions/zoom_behavior/
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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

