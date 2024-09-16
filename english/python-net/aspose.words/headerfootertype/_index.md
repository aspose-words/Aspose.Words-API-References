---
title: HeaderFooterType enumeration
linktitle: HeaderFooterType enumeration
articleTitle: HeaderFooterType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.HeaderFooterType enumeration. Identifies the type of header or footer found in a Word file."
type: docs
weight: 470
url: /python-net/aspose.words/headerfootertype/
---

## HeaderFooterType enumeration

Identifies the type of header or footer found in a Word file.


### Members

| Name | Description |
| --- | --- |
| HEADER_EVEN | Header for even numbered pages. |
| HEADER_PRIMARY | Primary header, also used for odd numbered pages. |
| FOOTER_EVEN | Footer for even numbered pages. |
| FOOTER_PRIMARY | Primary footer, also used for odd numbered pages. |
| HEADER_FIRST | Header for the first page of the section. |
| FOOTER_FIRST | Footer for the first page of the section. |

### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Specify that we want different headers and footers for first, even and odd pages.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Create the headers, then add three pages to the document to display each header type.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.write('Header for the first page')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.write('Header for even pages')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('Header for all other pages')
builder.move_to_section(0)
builder.writeln('Page1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page3')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.HeadersAndFooters.docx')
```

### See Also

* module [aspose.words](../)

