---
title: HtmlSaveOptions.export_headers_footers_mode property
linktitle: export_headers_footers_mode property
articleTitle: export_headers_footers_mode property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_headers_footers_mode property. Specifies how headers and footers are output to HTML, MHTML or EPUB"
type: docs
weight: 160
url: /es/python-net/aspose.words.saving/htmlsaveoptions/export_headers_footers_mode/
---

## HtmlSaveOptions.export_headers_footers_mode property

Specifies how headers and footers are output to HTML, MHTML or EPUB.
Default value is [ExportHeadersFootersMode.PER_SECTION](../../exportheadersfootersmode/#PER_SECTION) for HTML/MHTML
and [ExportHeadersFootersMode.NONE](../../exportheadersfootersmode/#NONE) for EPUB.



```python
@property
def export_headers_footers_mode(self) -> aspose.words.saving.ExportHeadersFootersMode:
    ...

@export_headers_footers_mode.setter
def export_headers_footers_mode(self, value: aspose.words.saving.ExportHeadersFootersMode):
    ...

```

### Remarks

It is hard to meaningfully output headers and footers to HTML because HTML is not paginated.

When this property is [ExportHeadersFootersMode.PER_SECTION](../../exportheadersfootersmode/#PER_SECTION), Aspose.Words exports
only primary headers and footers at the beginning and the end of each section.

When it is [ExportHeadersFootersMode.FIRST_SECTION_HEADER_LAST_SECTION_FOOTER](../../exportheadersfootersmode/#FIRST_SECTION_HEADER_LAST_SECTION_FOOTER)
only first primary header and the last primary footer (including linked to previous) are exported.

You can disable export of headers and footers altogether by setting this property
to [ExportHeadersFootersMode.NONE](../../exportheadersfootersmode/#NONE).




### Examples

Shows how to omit headers/footers when saving a document to HTML.

```python
doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
# Este documento contiene encabezados y pies de página. Podemos acceder a ellos mediante la colección "HeadersFooters".
self.assertEqual('First header', doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_FIRST).get_text().strip())
# Los formatos como .html no dividen el documento en páginas, por lo que los encabezados/pies de página no funcionarán de la misma manera
# como lo harían al abrir el documento como .docx usando Microsoft Word.
# Si convertimos un documento con encabezados/pies de página a html, la conversión incorporará los encabezados/pies de página al texto del cuerpo.
# Podemos usar un objeto SaveOptions para omitir los encabezados/pies de página al convertir a html.
save_options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
save_options.export_headers_footers_mode = aw.saving.ExportHeadersFootersMode.NONE
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.ExportMode.html', save_options=save_options)
# Abra nuestro documento guardado y verifique que no contenga el texto del encabezado.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HeaderFooter.ExportMode.html')
self.assertFalse('First header' in doc.range.text)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

