---
title: has_child_nodes property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns true if this node has any child nodes."
type: docs
weight: 40
url: /python-net/aspose.words/compositenode/has_child_nodes/
---

## CompositeNode.has_child_nodes property

Returns true if this node has any child nodes.


### Examples

Shows how to combine the rows from two tables into one.

```python
doc = aw.Document(MY_DIR + "Tables.docx")

# Below are two ways of getting a table from a document.
# 1 -  From the "tables" collection of a Body node:
first_table = doc.first_section.body.tables[0]

# 2 -  Using the "get_child" method:
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()

# Append all rows from the current table to the next.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)

# Remove the empty table container.
second_table.remove()

doc.save(ARTIFACTS_DIR + "Table.combine_tables.docx")
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

