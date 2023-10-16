---
title: DocumentBuilder.writeln method
linktitle: writeln method
articleTitle: writeln method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.writeln method"
type: docs
weight: 670
url: /python-net/aspose.words/documentbuilder/writeln/
---

## writeln(text) {#str}

Inserts a string and a paragraph break into the document.


```python
def writeln(self, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | str |  |

Current font and paragraph formatting specified by the [DocumentBuilder.font](../font/) and [DocumentBuilder.paragraph_format](../paragraph_format/) properties are used.



## writeln() {#default}

Inserts a paragraph break into the document.


```python
def writeln(self):
    ...
```

Calls [DocumentBuilder.insert_paragraph()](../insert_paragraph/#default).




## Examples

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

Shows how to build a formatted 2x2 table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.write("Row 1, cell 1.")
builder.insert_cell()
builder.write("Row 1, cell 2.")
builder.end_row()

# While building the table, the document builder will apply its current row_format/cell_format property values
# to the current row/cell that its cursor is in and any new rows/cells as it creates them.
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[0].cell_format.vertical_alignment)
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[1].cell_format.vertical_alignment)

builder.insert_cell()
builder.row_format.height = 100
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write("Row 2, cell 1.")
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write("Row 2, cell 2.")
builder.end_row()
builder.end_table()

# Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
self.assertEqual(aw.TextOrientation.UPWARD, table.rows[1].cells[0].cell_format.orientation)
self.assertEqual(aw.TextOrientation.DOWNWARD, table.rows[1].cells[1].cell_format.orientation)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.build_table.docx")
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

