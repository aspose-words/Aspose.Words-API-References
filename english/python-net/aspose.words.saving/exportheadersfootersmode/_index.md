---
title: ExportHeadersFootersMode enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies how headers and footers are exported to HTML, MHTML or EPUB."
type: docs
weight: 160
url: /python-net/aspose.words.saving/exportheadersfootersmode/
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
doc = aw.Document(MY_DIR + "Header and footer types.docx")

# This document contains headers and footers. We can access them via the "headers_footers" collection.
self.assertEqual("First header", doc.first_section.headers_footers[aw.HeaderFooterType.HEADER_FIRST].get_text().strip())

# Formats such as .html do not split the document into pages, so headers/footers will not function the same way
# they would when we open the document as a .docx using Microsoft Word.
# If we convert a document with headers/footers to html, the conversion will assimilate the headers/footers into body text.
# We can use a SaveOptions object to omit headers/footers while converting to html.
save_options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
save_options.export_headers_footers_mode = aw.saving.ExportHeadersFootersMode.NONE

doc.save(ARTIFACTS_DIR + "HeaderFooter.export_mode.html", save_options)

# Open our saved document and verify that it does not contain the header's text
doc = aw.Document(ARTIFACTS_DIR + "HeaderFooter.export_mode.html")

self.assertNotIn("First header", doc.range.text)
```

### See Also

* module [aspose.words.saving](../)
* property [HtmlSaveOptions.export_headers_footers_mode](../htmlsaveoptions/export_headers_footers_mode/)

