---
title: PdfSaveOptions.zoom_behavior property
linktitle: zoom_behavior property
articleTitle: zoom_behavior property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.zoom_behavior property. Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer."
type: docs
weight: 370
url: /fr/python-net/aspose.words.saving/pdfsaveoptions/zoom_behavior/
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
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
# Définissez la propriété "ZoomBehavior" sur "PdfZoomBehavior.ZoomFactor" pour que le lecteur PDF
# applique un facteur de zoom basé sur un pourcentage lorsque nous ouvrons le document avec celui-ci.
# Définissez la propriété "ZoomFactor" sur "25" pour donner au facteur de zoom une valeur de 25%.
options = aw.saving.PdfSaveOptions()
options.zoom_behavior = aw.saving.PdfZoomBehavior.ZOOM_FACTOR
options.zoom_factor = 25
# Lorsque nous ouvrons ce document avec un lecteur tel qu'Adobe Acrobat, nous verrons le document réduit à 1/4 de sa taille réelle.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ZoomBehaviour.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

