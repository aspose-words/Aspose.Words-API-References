---
title: Table.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Table.ensure_minimum method. If the table has no rows, creates and appends one [Row](../../row/)."
type: docs
weight: 400
url: /python-net/aspose.words.tables/table/ensure_minimum/
---

## ensure_minimum() {#default}

If the table has no rows, creates and appends one [Row](../../row/).



```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to ensure that a table node contains the nodes we need to add content.

```python
doc = aw.Document()
table = aw.tables.Table(doc)
doc.first_section.body.append_child(table)

# Tables contain rows, which contain cells, which may contain paragraphs
# with typical elements such as runs, shapes, and even other tables.
# Our new table has none of these nodes, and we cannot add contents to it until it does.
self.assertEqual(0, table.get_child_nodes(aw.NodeType.ANY, True).count)

# Calling the "ensure_minimum" method on a table will ensure that
# the table has at least one row and one cell with an empty paragraph.
table.ensure_minimum()
table.first_row.first_cell.first_paragraph.append_child(aw.Run(doc, "Hello world!"))
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

