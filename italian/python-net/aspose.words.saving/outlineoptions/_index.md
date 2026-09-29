---
title: OutlineOptions class
linktitle: OutlineOptions class
articleTitle: OutlineOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.OutlineOptions class. Allows to specify outline options"
type: docs
weight: 570
url: /it/python-net/aspose.words.saving/outlineoptions/
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

