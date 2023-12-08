---
title: Cell.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Cell.ensure_minimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 160
url: /python-net/aspose.words.tables/cell/ensure_minimum/
---

## ensure_minimum() {#default}

If the last child is not a paragraph, creates and appends one empty paragraph.


```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to ensure a cell node contains the nodes we need to begin adding content to it.

```python
doc = aw.Document()
table = aw.tables.Table(doc)
doc.first_section.body.append_child(table)
row = aw.tables.Row(doc)
table.append_child(row)
cell = aw.tables.Cell(doc)
row.append_child(cell)

# Cells may contain paragraphs with typical elements such as runs, shapes, and even other tables.
# Our new cell does not have any paragraphs, and we cannot add contents such as run and shape nodes to it until it does.
self.assertEqual(0, cell.get_child_nodes(aw.NodeType.ANY, True).count)

# Calling the "ensure_minimum" method on a cell will ensure that
# the cell has at least one empty paragraph, which we can then add contents to.
cell.ensure_minimum()
cell.first_paragraph.append_child(aw.Run(doc, "Hello world!"))
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

