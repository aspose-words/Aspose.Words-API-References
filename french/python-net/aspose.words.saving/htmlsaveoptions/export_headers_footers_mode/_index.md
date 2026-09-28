---
title: HtmlSaveOptions.export_headers_footers_mode property
linktitle: export_headers_footers_mode property
articleTitle: export_headers_footers_mode property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_headers_footers_mode property. Specifies how headers and footers are output to HTML, MHTML or EPUB"
type: docs
weight: 160
url: /fr/python-net/aspose.words.saving/htmlsaveoptions/export_headers_footers_mode/
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
# Ce document contient des en‑têtes et pieds de page. Nous pouvons y accéder via la collection "HeadersFooters".
self.assertEqual('First header', doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_FIRST).get_text().strip())
# Les formats tels que .html ne divisent pas le document en pages, de sorte que les en‑têtes/pieds de page ne fonctionneront pas de la même manière
# ce serait le cas lorsque nous ouvrons le document en .docx avec Microsoft Word.
# Si nous convertissons un document avec des en‑têtes/pieds de page en html, la conversion assimilera les en‑têtes/pieds de page au texte du corps.
# Nous pouvons utiliser un objet SaveOptions pour omettre les en‑têtes/pieds de page lors de la conversion en html.
save_options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
save_options.export_headers_footers_mode = aw.saving.ExportHeadersFootersMode.NONE
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.ExportMode.html', save_options=save_options)
# Ouvrez notre document enregistré et vérifiez qu'il ne contient pas le texte de l'en‑tête
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HeaderFooter.ExportMode.html')
self.assertFalse('First header' in doc.range.text)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

