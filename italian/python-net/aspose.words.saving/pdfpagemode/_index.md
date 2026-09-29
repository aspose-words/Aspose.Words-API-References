---
title: PdfPageMode enumeration
linktitle: PdfPageMode enumeration
articleTitle: PdfPageMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfPageMode enumeration. Specifies how the PDF document should be displayed when opened in the PDF reader."
type: docs
weight: 730
url: /it/python-net/aspose.words.saving/pdfpagemode/
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
save_options = aw.saving.PdfSaveOptions()
# Imposta la proprietà "PageMode" a "PdfPageMode.UseOutlines" per visualizzare il riquadro di navigazione dell'indice nel PDF di output.
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES
# Imposta la proprietà "DefaultBookmarksOutlineLevel" a "1" per visualizzare tutti i
# segnalibri al primo livello dell'indice nel PDF di output.
save_options.outline_options.default_bookmarks_outline_level = 1
# Imposta la proprietà "HeaderFooterBookmarksExportMode" a "HeaderFooterBookmarksExportMode.None" per
# non esportare alcun segnalibro presente nelle intestazioni/piè di pagina.
# Imposta la proprietà "HeaderFooterBookmarksExportMode" a "HeaderFooterBookmarksExportMode.First" per
# esportare solo i segnalibri nelle intestazioni/piè di pagina della prima sezione.
# Imposta la proprietà "HeaderFooterBookmarksExportMode" a "HeaderFooterBookmarksExportMode.All" per
# esportare i segnalibri presenti in tutte le intestazioni/piè di pagina.
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

