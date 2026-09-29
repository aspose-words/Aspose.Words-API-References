---
title: OutlineOptions class
linktitle: OutlineOptions class
articleTitle: OutlineOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.OutlineOptions class. Allows to specify outline options"
type: docs
weight: 570
url: /es/python-net/aspose.words.saving/outlineoptions/
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
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
save_options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "PageMode" a "PdfPageMode.UseOutlines" para mostrar el panel de navegación del esquema en el PDF de salida.
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES
# Establezca la propiedad "DefaultBookmarksOutlineLevel" a "1" para mostrar todos los
# marcadores en el primer nivel del esquema en el PDF de salida.
save_options.outline_options.default_bookmarks_outline_level = 1
# Establezca la propiedad "HeaderFooterBookmarksExportMode" a "HeaderFooterBookmarksExportMode.None" para
# no exportar ningún marcador que esté dentro de encabezados/pies de página.
# Establezca la propiedad "HeaderFooterBookmarksExportMode" a "HeaderFooterBookmarksExportMode.First" para
# exportar solo los marcadores en los encabezados/pies de página de la primera sección.
# Establezca la propiedad "HeaderFooterBookmarksExportMode" a "HeaderFooterBookmarksExportMode.All" para
# exportar los marcadores que están en todos los encabezados/pies de página.
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

