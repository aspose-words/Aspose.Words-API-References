---
title: NodeCollection.index_of method
linktitle: index_of method
articleTitle: index_of method
second_title: Aspose.Words for Python
description: "NodeCollection.index_of method. Returns the zero-based index of the specified node."
type: docs
weight: 60
url: /python-net/aspose.words/nodecollection/index_of/
---

## index_of(node) {#node}

Returns the zero-based index of the specified node.


```python
def index_of(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node to locate. |

### Remarks

This method performs a linear search; therefore, the average execution time is proportional to [NodeCollection.count](../count/).




### Returns

The zero-based index of the node within the collection, if found; otherwise, -1.


### Examples

Shows how to get the index of a node in a collection.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
all_tables = doc.get_child_nodes(aw.NodeType.TABLE, True)
self.assertEqual(0, all_tables.index_of(table))
row = table.rows[2]
self.assertEqual(2, table.index_of(row))
cell = row.last_cell
self.assertEqual(4, row.index_of(cell))
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

