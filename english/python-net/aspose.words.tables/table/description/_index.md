---
title: description property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets description of this table"
type: docs
weight: 110
url: /python-net/aspose.words.tables/table/description/
---

## Table.description property

Gets or sets description of this table.
It provides an alternative text representation of the information contained in the table.

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents
([OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)).
When saved to pre-ISO/IEC 29500 formats, the property is ignored.




### Examples

Shows how to build a nested table without using a document builder.

```python
def test_create_nested_table(self):

    doc = aw.Document()

    # Create the outer table with three rows and four columns, and then add it to the document.
    outer_table = ExTable.create_table(doc, 3, 4, "Outer Table")
    doc.first_section.body.append_child(outer_table)

    # Create another table with two rows and two columns and then insert it into the first table's first cell.
    inner_table = ExTable.create_table(doc, 2, 2, "Inner Table")
    outer_table.first_row.first_cell.append_child(inner_table)

    doc.save(ARTIFACTS_DIR + "Table.create_nested_table.docx")

@staticmethod
def create_table(doc: aw.Document, row_count: int, cell_count: int, cell_text: str) -> aw.tables.Table:
    """Creates a new table in the document with the given dimensions and text in each cell."""
    table = aw.tables.Table(doc)

    for row_id in range(1, row_count + 1):
        row = aw.tables.Row(doc)
        table.append_child(row)

        for cell_id in range(1, cell_count + 1):
            cell = aw.tables.Cell(doc)
            cell.append_child(aw.Paragraph(doc))
            cell.first_paragraph.append_child(aw.Run(doc, cell_text))

            row.append_child(cell)

    # You can use the "title" and "description" properties to add a title and description respectively to your table.
    # The table must have at least one row before we can use these properties.
    # These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
    # If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
    table.title = "Aspose table title"
    table.description = "Aspose table description"

    return table
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

