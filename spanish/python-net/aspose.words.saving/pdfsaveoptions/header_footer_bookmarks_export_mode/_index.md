---
title: PdfSaveOptions.header_footer_bookmarks_export_mode property
linktitle: header_footer_bookmarks_export_mode property
articleTitle: header_footer_bookmarks_export_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.header_footer_bookmarks_export_mode property. Determines how bookmarks in headers/footers are exported."
type: docs
weight: 200
url: /es/python-net/aspose.words.saving/pdfsaveoptions/header_footer_bookmarks_export_mode/
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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

