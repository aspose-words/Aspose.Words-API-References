---
title: Table constructor
linktitle: Table constructor
articleTitle: Table constructor
second_title: Aspose.Words for Python
description: "Table constructor. Initializes a new instance of the [Table](../) class."
type: docs
weight: 10
url: /python-net/aspose.words.tables/table/__init__/
---

## Table(doc) {#documentbase}

Initializes a new instance of the [Table](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |

### Remarks

When [Table](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../../aspose.words/node/parent_node/) is ``None``.

To append [Table](../) to the document use [CompositeNode.insert_after()](../../../aspose.words/compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../../aspose.words/compositenode/insert_before/#node_node)
on the story where you want the table inserted.




### Examples

Shows how to create a table.

```python
doc = aw.Document()
table = aw.tables.Table(doc)
doc.first_section.body.append_child(table)

# Tables contain rows, which contain cells, which may have paragraphs
# with typical elements such as runs, shapes, and even other tables.
# Calling the "ensure_minimum" method on a table will ensure that
# the table has at least one row, cell, and paragraph.
first_row = aw.tables.Row(doc)
table.append_child(first_row)

first_cell = aw.tables.Cell(doc)
first_row.append_child(first_cell)

paragraph = aw.Paragraph(doc)
first_cell.append_child(paragraph)

# Add text to the first cell in the first row of the table.
run = aw.Run(doc, "Hello world!")
paragraph.append_child(run)

doc.save(ARTIFACTS_DIR + "Table.create_table.docx")
```

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

