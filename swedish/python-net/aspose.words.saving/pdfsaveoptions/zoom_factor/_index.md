---
title: PdfSaveOptions.zoom_factor property
linktitle: zoom_factor property
articleTitle: zoom_factor property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.zoom_factor property. Gets or sets a value determining zoom factor (in percentages) for a document."
type: docs
weight: 380
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/zoom_factor/
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
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
# Ställ in egenskapen "ZoomBehavior" till "PdfZoomBehavior.ZoomFactor" för att få en PDF-läsare att
# tillämpa en procentbaserad zoomfaktor när vi öppnar dokumentet med den.
# Ställ in egenskapen "ZoomFactor" till "25" för att ge zoomfaktorn värdet 25%.
options = aw.saving.PdfSaveOptions()
options.zoom_behavior = aw.saving.PdfZoomBehavior.ZOOM_FACTOR
options.zoom_factor = 25
# När vi öppnar detta dokument med en läsare som Adobe Acrobat kommer vi att se dokumentet skalat till 1/4 av dess faktiska storlek.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ZoomBehaviour.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

