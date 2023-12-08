---
title: PdfZoomBehavior enumeration
linktitle: PdfZoomBehavior enumeration
articleTitle: PdfZoomBehavior enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfZoomBehavior enumeration. Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer."
type: docs
weight: 700
url: /python-net/aspose.words.saving/pdfzoombehavior/
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
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
# Set the "zoom_behavior" property to "PdfZoomBehavior.ZOOM_FACTOR" to get a PDF reader to
# apply a percentage-based zoom factor when we open the document with it.
# Set the "zoom_factor" property to "25" to give the zoom factor a value of 25%.
options = aw.saving.PdfSaveOptions()
options.zoom_behavior = aw.saving.PdfZoomBehavior.ZOOM_FACTOR
options.zoom_factor = 25

# When we open this document using a reader such as Adobe Acrobat, we will see the document scaled at 1/4 of its actual size.
doc.save(ARTIFACTS_DIR + "PdfSaveOptions.zoom_behaviour.pdf", options)
```

### See Also

* module [aspose.words.saving](../)

