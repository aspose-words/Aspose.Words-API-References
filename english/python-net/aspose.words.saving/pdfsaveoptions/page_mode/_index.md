---
title: PdfSaveOptions.page_mode property
linktitle: page_mode property
articleTitle: page_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.page_mode property. Specifies how the PDF document should be displayed when opened in a PDF reader."
type: docs
weight: 260
url: /python-net/aspose.words.saving/pdfsaveoptions/page_mode/
---

## PdfSaveOptions.page_mode property

Specifies how the PDF document should be displayed when opened in a PDF reader.


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
doc = aw.Document(file_name=MY_DIR + 'Bookmarks in headers and footers.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()
# Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES
# Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
# bookmarks at the first level of the outline in the output PDF.
save_options.outline_options.default_bookmarks_outline_level = 1
# Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
# not export any bookmarks that are inside headers/footers.
# Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
# only export bookmarks in the first section's header/footers.
# Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
# export bookmarks that are in all headers/footers.
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

