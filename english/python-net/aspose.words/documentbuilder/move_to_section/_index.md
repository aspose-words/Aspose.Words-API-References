---
title: DocumentBuilder.move_to_section method
linktitle: move_to_section method
articleTitle: move_to_section method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_section method. Moves the cursor to the beginning of the body in a specified section."
type: docs
weight: 580
url: /python-net/aspose.words/documentbuilder/move_to_section/
---

## move_to_section(section_index) {#int}

Moves the cursor to the beginning of the body in a specified section.


```python
def move_to_section(self, section_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| section_index | int | The index of the section to move to. |

### Remarks

When *sectionIndex* is greater than or equal to 0, it specifies an index from
the beginning of the document with 0 being the first section. When*sectionIndex* is less than 0,
it specified an index from the end of the document with -1 being the last section.

The cursor is moved to the first paragraph in the [Body](../../body/) of the specified section.




### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Specify that we want different headers and footers for first, even and odd pages.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True

# Create the headers, then add three pages to the document to display each header type.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.write("Header for the first page")
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.write("Header for even pages")
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write("Header for all other pages")

builder.move_to_section(0)
builder.writeln("Page1")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page2")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page3")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.headers_and_footers.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

