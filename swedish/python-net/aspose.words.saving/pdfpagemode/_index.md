---
title: PdfPageMode enumeration
linktitle: PdfPageMode enumeration
articleTitle: PdfPageMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfPageMode enumeration. Specifies how the PDF document should be displayed when opened in the PDF reader."
type: docs
weight: 730
url: /sv/python-net/aspose.words.saving/pdfpagemode/
---

## PdfPageMode enumeration

Specifies how the PDF document should be displayed when opened in the PDF reader.


### Members

| Name | Description |
| --- | --- |
| USE_NONE | Neither document outline nor thumbnail images are visible. |
| USE_OUTLINES | Document outline is visible. Note that if there're no outlines in the PDF document then outline navigation pane will not be visible anyway. |
| USE_THUMBS | Thumbnail images are visible. |
| FULL_SCREEN | Full-screen mode, with no menu bar, window controls, or any other window visible. |
| USE_OC | Optional content group panel is visible. |
| USE_ATTACHMENTS | Attachments panel is visible. |

### Examples

Shows to process bookmarks in headers/footers in a document that we are rendering to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'Bookmarks in headers and footers.docx')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
save_options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "PageMode" till "PdfPageMode.UseOutlines" för att visa konturens navigationspanel i den genererade PDF-filen.
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES
# Ställ in egenskapen "DefaultBookmarksOutlineLevel" till "1" för att visa alla
# bokmärken på den första nivån i konturen i den genererade PDF-filen.
save_options.outline_options.default_bookmarks_outline_level = 1
# Ställ in egenskapen "HeaderFooterBookmarksExportMode" till "HeaderFooterBookmarksExportMode.None" för att
# inte exportera några bokmärken som finns i sidhuvuden/sidfötter.
# Ställ in egenskapen "HeaderFooterBookmarksExportMode" till "HeaderFooterBookmarksExportMode.First" för att
# endast exportera bokmärken i den första sektionens sidhuvuden/sidfötter.
# Ställ in egenskapen "HeaderFooterBookmarksExportMode" till "HeaderFooterBookmarksExportMode.All" för att
# exportera bokmärken som finns i alla sidhuvuden/sidfötter.
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

