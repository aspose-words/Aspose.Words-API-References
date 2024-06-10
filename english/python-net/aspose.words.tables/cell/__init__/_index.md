---
title: Cell constructor
linktitle: Cell constructor
articleTitle: Cell constructor
second_title: Aspose.Words for Python
description: "Cell constructor. Initializes a new instance of the [Cell](../) class."
type: docs
weight: 10
url: /python-net/aspose.words.tables/cell/__init__/
---

## Cell(doc) {#documentbase}

Initializes a new instance of the [Cell](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |

### Remarks

When [Cell](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../../aspose.words/node/parent_node/) is ``None``.

To append [Cell](../) to the document use [CompositeNode.insert_after()](../../../aspose.words/compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../../aspose.words/compositenode/insert_before/#node_node)
on the row where you want the cell inserted.




### Examples

Shows how to build a nested table without using a document builder.

```python
def create_nested_table():
    doc = aw.Document()
    # Create the outer table with three rows and four columns, and then add it to the document.
    outer_table = create_table(doc, 3, 4, 'Outer Table')
    doc.first_section.body.append_child(outer_table)
    # Create another table with two rows and two columns and then insert it into the first table's first cell.
    inner_table = create_table(doc, 2, 2, 'Inner Table')
    outer_table.first_row.first_cell.append_child(inner_table)
    doc.save(ARTIFACTS_DIR + 'Table.create_nested_table.docx')

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
    table.title = 'Aspose table title'
    table.description = 'Aspose table description'
    return table
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

