---
title: OutlineOptions class
linktitle: OutlineOptions class
articleTitle: OutlineOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.OutlineOptions class. Allows to specify outline options"
type: docs
weight: 540
url: /python-net/aspose.words.saving/outlineoptions/
---

## OutlineOptions class

Allows to specify outline options.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [OutlineOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmarks_outline_levels](./bookmarks_outline_levels/) | Allows to specify individual bookmarks outline level. |
| [create_missing_outline_levels](./create_missing_outline_levels/) | Gets or sets a value determining whether or not to create missing outline levels when the document is  exported. |
| [create_outlines_for_headings_in_tables](./create_outlines_for_headings_in_tables/) | Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables. |
| [default_bookmarks_outline_level](./default_bookmarks_outline_level/) | Specifies the default level in the document outline at which to display Word bookmarks. |
| [expanded_outline_levels](./expanded_outline_levels/) | Specifies how many levels in the document outline to show expanded when the file is viewed. |
| [headings_outline_levels](./headings_outline_levels/) | Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the  document outline. |

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

* module [aspose.words.saving](../)

