---
title: PdfSaveOptions.page_mode property
linktitle: page_mode property
articleTitle: page_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.page_mode property. Specifies how the PDF document should be displayed when opened in a PDF reader."
type: docs
weight: 280
url: /es/python-net/aspose.words.saving/pdfsaveoptions/page_mode/
---

## PdfSaveOptions.page_mode property

Specifies how the PDF document should be displayed when opened in a PDF reader.


```python
@property
def page_mode(self) -> aspose.words.saving.PdfPageMode:
    ...

@page_mode.setter
def page_mode(self, value: aspose.words.saving.PdfPageMode):
    ...

```

### Remarks

The default value is [PdfPageMode.USE_OUTLINES](../../pdfpagemode/#USE_OUTLINES).



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

