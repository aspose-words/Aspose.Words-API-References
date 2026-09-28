---
title: PdfPageMode enumeration
linktitle: PdfPageMode enumeration
articleTitle: PdfPageMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfPageMode enumeration. Specifies how the PDF document should be displayed when opened in the PDF reader."
type: docs
weight: 730
url: /de/python-net/aspose.words.saving/pdfpagemode/
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
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
save_options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "PageMode" auf "PdfPageMode.UseOutlines", um das Gliederungs‑Navigationsfenster im ausgegebenen PDF anzuzeigen.
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES
# Setzen Sie die Eigenschaft "DefaultBookmarksOutlineLevel" auf "1", um alle
# Lesezeichen auf der ersten Ebene der Gliederung im ausgegebenen PDF anzuzeigen.
save_options.outline_options.default_bookmarks_outline_level = 1
# Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.None", um
# keine Lesezeichen zu exportieren, die sich in Kopf‑/Fußzeilen befinden.
# Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.First", um
# nur Lesezeichen im Kopf‑/Fußzeilenbereich des ersten Abschnitts zu exportieren.
# Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.All", um
# Lesezeichen zu exportieren, die sich in allen Kopf‑/Fußzeilen befinden.
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

