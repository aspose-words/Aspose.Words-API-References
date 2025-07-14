---
title: PdfSaveOptions.zoom_factor property
linktitle: zoom_factor property
articleTitle: zoom_factor property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.zoom_factor property. Gets or sets a value determining zoom factor (in percentages) for a document."
type: docs
weight: 360
url: /python-net/aspose.words.saving/pdfsaveoptions/zoom_factor/
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
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
# Set the "ZoomBehavior" property to "PdfZoomBehavior.ZoomFactor" to get a PDF reader to
# apply a percentage-based zoom factor when we open the document with it.
# Set the "ZoomFactor" property to "25" to give the zoom factor a value of 25%.
options = aw.saving.PdfSaveOptions()
options.zoom_behavior = aw.saving.PdfZoomBehavior.ZOOM_FACTOR
options.zoom_factor = 25
# When we open this document using a reader such as Adobe Acrobat, we will see the document scaled at 1/4 of its actual size.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ZoomBehaviour.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

