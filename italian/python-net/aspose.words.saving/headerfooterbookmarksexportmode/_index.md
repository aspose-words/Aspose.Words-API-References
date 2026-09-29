---
title: HeaderFooterBookmarksExportMode enumeration
linktitle: HeaderFooterBookmarksExportMode enumeration
articleTitle: HeaderFooterBookmarksExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.HeaderFooterBookmarksExportMode enumeration. Specifies how bookmarks in headers/footers are exported."
type: docs
weight: 220
url: /it/python-net/aspose.words.saving/headerfooterbookmarksexportmode/
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

