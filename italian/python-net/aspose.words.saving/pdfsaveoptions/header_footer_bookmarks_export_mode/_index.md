---
title: PdfSaveOptions.header_footer_bookmarks_export_mode property
linktitle: header_footer_bookmarks_export_mode property
articleTitle: header_footer_bookmarks_export_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.header_footer_bookmarks_export_mode property. Determines how bookmarks in headers/footers are exported."
type: docs
weight: 200
url: /it/python-net/aspose.words.saving/pdfsaveoptions/header_footer_bookmarks_export_mode/
---

## PdfSaveOptions.header_footer_bookmarks_export_mode property

Determines how bookmarks in headers/footers are exported.


```python
@property
def header_footer_bookmarks_export_mode(self) -> aspose.words.saving.HeaderFooterBookmarksExportMode:
    ...

@header_footer_bookmarks_export_mode.setter
def header_footer_bookmarks_export_mode(self, value: aspose.words.saving.HeaderFooterBookmarksExportMode):
    ...

```

### Remarks

The default value is [HeaderFooterBookmarksExportMode.ALL](../../headerfooterbookmarksexportmode/#ALL).

This property is used in conjunction with the [PdfSaveOptions.outline_options](../outline_options/) option.




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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

