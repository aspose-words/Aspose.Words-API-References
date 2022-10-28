---
title: zoom_factor property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a value determining zoom factor (in percentages) for a document."
type: docs
weight: 320
url: /python-net/aspose.words.saving/pdfsaveoptions/zoom_factor/
---

## PdfSaveOptions.zoom_factor property

Gets or sets a value determining zoom factor (in percentages) for a document.

This value is used only if [PdfSaveOptions.zoom_behavior](../zoom_behavior/) is set to [PdfZoomBehavior.ZOOM_FACTOR](../../pdfzoombehavior/#ZOOM_FACTOR).



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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

