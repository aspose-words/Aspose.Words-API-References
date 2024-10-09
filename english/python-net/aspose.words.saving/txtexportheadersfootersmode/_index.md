---
title: TxtExportHeadersFootersMode enumeration
linktitle: TxtExportHeadersFootersMode enumeration
articleTitle: TxtExportHeadersFootersMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TxtExportHeadersFootersMode enumeration. Specifies the way headers and footers are exported to plain text format."
type: docs
weight: 820
url: /python-net/aspose.words.saving/txtexportheadersfootersmode/
---

## TxtExportHeadersFootersMode enumeration

Specifies the way headers and footers are exported to plain text format.


### Members

| Name | Description |
| --- | --- |
| NONE | No headers and footers are exported. |
| PRIMARY_ONLY | Only primary headers and footers are exported at the beginning and end of each section. |
| ALL_AT_END | All headers and footers are placed after all section bodies at the very end of a document. |

### Examples

Shows how to specify how to export headers and footers to plain text format.

```python
doc = aw.Document()
# Insert even and primary headers/footers into the document.
# The primary header/footers will override the even headers/footers.
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_EVEN))
doc.first_section.headers_footers.header_even.append_paragraph('Even header')
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.FOOTER_EVEN))
doc.first_section.headers_footers.footer_even.append_paragraph('Even footer')
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY))
doc.first_section.headers_footers.header_primary.append_paragraph('Primary header')
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.FOOTER_PRIMARY))
doc.first_section.headers_footers.footer_primary.append_paragraph('Primary footer')
# Insert pages to display these headers and footers.
builder = aw.DocumentBuilder(doc)
builder.writeln('Page 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Page 3')
# Create a "TxtSaveOptions" object, which we can pass to the document's "save" method
# to modify how we save the document to plaintext.
save_options = aw.saving.TxtSaveOptions()
# Set the "export_headers_footers_mode" property to "TxtExportHeadersFootersMode.NONE"
# to not export any headers/footers.
# Set the "export_headers_footers_mode" property to "TxtExportHeadersFootersMode.PRIMARY_ONLY"
# to only export primary headers/footers.
# Set the "export_headers_footers_mode" property to "TxtExportHeadersFootersMode.ALL_AT_END"
# to place all headers and footers for all section bodies at the end of the document.
save_options.export_headers_footers_mode = txt_export_headers_footers_mode
doc.save(ARTIFACTS_DIR + 'TxtSaveOptions.export_headers_footers.txt', save_options)
with open(ARTIFACTS_DIR + 'TxtSaveOptions.export_headers_footers.txt', 'rb') as file:
    doc_text = file.read().decode('utf-8-sig')
if txt_export_headers_footers_mode == aw.saving.TxtExportHeadersFootersMode.ALL_AT_END:
    self.assertEqual('Page 1\r\n' + 'Page 2\r\n' + 'Page 3\r\n' + 'Even header\r\n\r\n' + 'Primary header\r\n\r\n' + 'Even footer\r\n\r\n' + 'Primary footer\r\n\r\n', doc_text)
elif txt_export_headers_footers_mode == aw.saving.TxtExportHeadersFootersMode.PRIMARY_ONLY:
    self.assertEqual('Primary header\r\n' + 'Page 1\r\n' + 'Page 2\r\n' + 'Page 3\r\n' + 'Primary footer\r\n', doc_text)
elif txt_export_headers_footers_mode == aw.saving.TxtExportHeadersFootersMode.NONE:
    self.assertEqual('Page 1\r\n' + 'Page 2\r\n' + 'Page 3\r\n', doc_text)
```

### See Also

* module [aspose.words.saving](../)

