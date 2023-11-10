---
title: RowFormat.heading_format property
linktitle: heading_format property
articleTitle: heading_format property
second_title: Aspose.Words for Python
description: "RowFormat.heading_format property. True if the row is repeated as a table heading on every page when the table spans more than one page."
type: docs
weight: 30
url: /python-net/aspose.words.tables/rowformat/heading_format/
---

## RowFormat.heading_format property

True if the row is repeated as a table heading on every page when the table spans more than one page.


```python
@property
def heading_format(self) -> bool:
    ...

@heading_format.setter
def heading_format(self, value: bool):
    ...

```

### Examples

Shows how to build a table with rows that repeat on every page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()

# Any rows inserted while the "heading_format" flag is set to "True"
# will show up at the top of the table on every page that it spans.
builder.row_format.heading_format = True
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.cell_format.width = 100
builder.insert_cell()
builder.write("Heading row 1")
builder.end_row()
builder.insert_cell()
builder.write("Heading row 2")
builder.end_row()

builder.cell_format.width = 50
builder.paragraph_format.clear_formatting()
builder.row_format.heading_format = False

# Add enough rows for the table to span two pages.
for i in range(50):
    builder.insert_cell()
    builder.write(f"Row {table.rows.count}, column 1.")
    builder.insert_cell()
    builder.write(f"Row {table.rows.count}, column 2.")
    builder.end_row()

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_table_set_heading_row.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [RowFormat](../)

