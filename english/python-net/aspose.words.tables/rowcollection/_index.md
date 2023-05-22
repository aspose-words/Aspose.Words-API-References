﻿---
title: RowCollection class
linktitle: RowCollection class
articleTitle: RowCollection class
second_title: Aspose.Words for Python
description: "aspose.words.tables.RowCollection class. Provides typed access to a collection of [Row](../row/) nodes"
type: docs
weight: 100
url: /python-net/aspose.words.tables/rowcollection/
---

## RowCollection class

Provides typed access to a collection of [Row](../row/) nodes.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/python-net/working-with-tables/) documentation article.




**Inheritance:** [RowCollection](./) → [NodeCollection](../../aspose.words/nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Row](../row/) at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](../../aspose.words/nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../../aspose.words/nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ clear()](../../aspose.words/nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ contains(node)](../../aspose.words/nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ index_of(node)](../../aspose.words/nodecollection/index_of/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ insert(index, node)](../../aspose.words/nodecollection/insert/#int_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ remove(node)](../../aspose.words/nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ remove_at(index)](../../aspose.words/nodecollection/remove_at/#int) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../../aspose.words/nodecollection/)) |
|[ to_array()](./to_array/#default) | Copies all rows from the collection to a new array of rows. |

### Examples

Shows how to iterate through all tables in the document and print the contents of each cell.

```python
doc = aw.Document(MY_DIR + "Tables.docx")
tables = doc.first_section.body.tables

self.assertEqual(2, len(tables.to_array()))

for i in range(tables.count):
    print("Start of Table", i)

    rows = tables[i].rows

    # We can use the "to_array" method on a row collection to clone it into an array.
    self.assertSequenceEqual(list(rows), rows.to_array())
    #Assert.are_not_same(rows, rows.to_array())

    for j in range(rows.count):
        print("\tStart of Row", j)

        cells = rows[j].cells

        # We can use the "to_array" method on a cell collection to clone it into an array.
        self.assertSequenceEqual(list(cells), cells.to_array())
        #Assert.are_not_same(cells, cells.to_array())

        for k in range(cells.count):
            cell_text = cells[k].to_string(aw.SaveFormat.TEXT).strip()
            print(f"\t\tContents of Cell:{k} = \"{cell_text}\"")

        print(f"\tEnd of Row {j}")

    print(f"End of Table {i}\n")
```

### See Also

* module [aspose.words.tables](../)
* class [NodeCollection](../../aspose.words/nodecollection/)

