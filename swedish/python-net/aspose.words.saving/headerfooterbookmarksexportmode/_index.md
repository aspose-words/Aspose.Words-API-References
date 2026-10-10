---
title: HeaderFooterBookmarksExportMode enumeration
linktitle: HeaderFooterBookmarksExportMode enumeration
articleTitle: HeaderFooterBookmarksExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.HeaderFooterBookmarksExportMode enumeration. Specifies how bookmarks in headers/footers are exported."
type: docs
weight: 220
url: /sv/python-net/aspose.words.saving/headerfooterbookmarksexportmode/
---

## HeaderFooterBookmarksExportMode enumeration

Specifies how bookmarks in headers/footers are exported.


### Members

| Name | Description |
| --- | --- |
| NONE | Bookmarks in headers/footers are not exported. |
| FIRST | Only bookmark in first header/footer of the section is exported. |
| ALL | Bookmarks in all headers/footers are exported. |

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

