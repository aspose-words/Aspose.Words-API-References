---
title: HeaderFooterBookmarksExportMode enumeration
linktitle: HeaderFooterBookmarksExportMode enumeration
articleTitle: HeaderFooterBookmarksExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.HeaderFooterBookmarksExportMode enumeration. Specifies how bookmarks in headers/footers are exported."
type: docs
weight: 220
url: /es/python-net/aspose.words.saving/headerfooterbookmarksexportmode/
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

