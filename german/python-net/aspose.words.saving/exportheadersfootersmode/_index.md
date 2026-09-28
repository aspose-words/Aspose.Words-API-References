---
title: ExportHeadersFootersMode enumeration
linktitle: ExportHeadersFootersMode enumeration
articleTitle: ExportHeadersFootersMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ExportHeadersFootersMode enumeration. Specifies how headers and footers are exported to HTML, MHTML or EPUB."
type: docs
weight: 180
url: /de/python-net/aspose.words.saving/exportheadersfootersmode/
---

## ExportHeadersFootersMode enumeration

Specifies how headers and footers are exported to HTML, MHTML or EPUB.


### Members

| Name | Description |
| --- | --- |
| NONE | Headers and footers are not exported. |
| PER_SECTION | Primary headers and footers are exported at the beginning and the end of each section. |
| FIRST_SECTION_HEADER_LAST_SECTION_FOOTER | Primary header of the first section is exported at the beginning of the document and primary footer is at the end. |
| FIRST_PAGE_HEADER_FOOTER_PER_SECTION | First page header and footer are exported at the beginning and the end of each section. |

### Examples

Shows how to omit headers/footers when saving a document to HTML.

```python
doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
# Dieses Dokument enthält Kopf- und Fußzeilen. Wir können über die "HeadersFooters"-Sammlung darauf zugreifen.
self.assertEqual('First header', doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_FIRST).get_text().strip())
# Formate wie .html teilen das Dokument nicht in Seiten auf, sodass Kopf‑/Fußzeilen nicht auf dieselbe Weise funktionieren.
# wie sie es tun würden, wenn wir das Dokument als .docx mit Microsoft Word öffnen.
# Wenn wir ein Dokument mit Kopf‑/Fußzeilen nach html konvertieren, wird die Konvertierung die Kopf‑/Fußzeilen in den Fließtext integrieren.
# Wir können ein SaveOptions‑Objekt verwenden, um Kopf‑/Fußzeilen beim Konvertieren nach html zu weglassen.
save_options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
save_options.export_headers_footers_mode = aw.saving.ExportHeadersFootersMode.NONE
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.ExportMode.html', save_options=save_options)
# Öffnen Sie unser gespeichertes Dokument und prüfen Sie, dass es den Text der Kopfzeile nicht enthält
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HeaderFooter.ExportMode.html')
self.assertFalse('First header' in doc.range.text)
```

### See Also

* module [aspose.words.saving](../)
* property [HtmlSaveOptions.export_headers_footers_mode](../htmlsaveoptions/export_headers_footers_mode/)

