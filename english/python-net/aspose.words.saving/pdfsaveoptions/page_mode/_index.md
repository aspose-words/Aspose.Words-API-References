---
title: PdfSaveOptions.page_mode property
linktitle: page_mode property
articleTitle: page_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.page_mode property. Specifies how the PDF document should be displayed when opened in the PDF reader."
type: docs
weight: 250
url: /python-net/aspose.words.saving/pdfsaveoptions/page_mode/
---

## PdfSaveOptions.page_mode property

Specifies how the PDF document should be displayed when opened in the PDF reader.


```python
@property
def page_mode(self) -> aspose.words.saving.PdfPageMode:
    ...

@page_mode.setter
def page_mode(self, value: aspose.words.saving.PdfPageMode):
    ...

```

### Remarks

The default value is [PdfPageMode.USE_OUTLINES](../../pdfpagemode/#USE_OUTLINES).



### Examples

Shows to process bookmarks in headers/footers in a document that we are rendering to PDF.

```python
doc = aw.Document(MY_DIR + "Bookmarks in headers and footers.docx")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()

# Set the "page_mode" property to "PdfPageMode.USE_OUTLINES" to display the outline navigation pane in the output PDF.
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES

# Set the "default_bookmarks_outline_level" property to "1" to display all
# bookmarks at the first level of the outline in the output PDF.
save_options.outline_options.default_bookmarks_outline_level = 1

# Set the "header_footer_bookmarks_export_mode" property to "HeaderFooterBookmarksExportMode.NONE" to
# not export any bookmarks that are inside headers/footers.
# Set the "header_footer_bookmarks_export_mode" property to "HeaderFooterBookmarksExportMode.FIRST" to
# only export bookmarks in the first section's header/footers.
# Set the "header_footer_bookmarks_export_mode" property to "HeaderFooterBookmarksExportMode.ALL" to
# export bookmarks that are in all headers/footers.
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.header_footer_bookmarks_export_mode.pdf", save_options)
```

Shows how to set instructions for some PDF readers to follow when opening an output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Set the "page_mode" property to "PdfPageMode.FULL_SCREEN" to get the PDF reader to open the saved
# document in full-screen mode, which takes over the monitor's display and has no controls visible.
# Set the "page_mode" property to "PdfPageMode.USE_THUMBS" to get the PDF reader to display a separate panel
# with a thumbnail for each page in the document.
# Set the "page_mode" property to "PdfPageMode.USE_OC" to get the PDF reader to display a separate panel
# that allows us to work with any layers present in the document.
# Set the "page_mode" property to "PdfPageMode.USE_OUTLINES" to get the PDF reader
# also to display the outline, if possible.
# Set the "page_mode" property to "PdfPageMode.USE_NONE" to get the PDF reader to display just the document itself.
# Set the "page_mode" property to "PdfPageMode.USE_ATTACHMENTS" to make visible attachments panel.
options.page_mode = page_mode

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.page_mode.pdf", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

