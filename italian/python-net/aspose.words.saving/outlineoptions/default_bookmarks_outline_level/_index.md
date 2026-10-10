---
title: OutlineOptions.default_bookmarks_outline_level property
linktitle: default_bookmarks_outline_level property
articleTitle: default_bookmarks_outline_level property
second_title: Aspose.Words for Python
description: "OutlineOptions.default_bookmarks_outline_level property. Specifies the default level in the document outline at which to display Word bookmarks."
type: docs
weight: 50
url: /it/python-net/aspose.words.saving/outlineoptions/default_bookmarks_outline_level/
---

## OutlineOptions.default_bookmarks_outline_level property

Specifies the default level in the document outline at which to display Word bookmarks.


```python
@property
def default_bookmarks_outline_level(self) -> int:
    ...

@default_bookmarks_outline_level.setter
def default_bookmarks_outline_level(self, value: int):
    ...

```

### Remarks

Individual bookmarks level could be specified using [OutlineOptions.bookmarks_outline_levels](../bookmarks_outline_levels/) property.

Specify 0 and Word bookmarks will not be displayed in the document outline.
Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.




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
* class [OutlineOptions](../)

