---
title: PdfPageMode enumeration
linktitle: PdfPageMode enumeration
articleTitle: PdfPageMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfPageMode enumeration. Specifies how the PDF document should be displayed when opened in the PDF reader."
type: docs
weight: 730
url: /es/python-net/aspose.words.saving/pdfpagemode/
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

