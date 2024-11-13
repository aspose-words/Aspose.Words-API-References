---
title: CellCollection class
linktitle: CellCollection class
articleTitle: CellCollection class
second_title: Aspose.Words for Python
description: "aspose.words.tables.CellCollection class. Provides typed access to a collection of [Cell](../cell/) nodes"
type: docs
weight: 30
url: /python-net/aspose.words.tables/cellcollection/
---

## CellCollection class

Provides typed access to a collection of [Cell](../cell/) nodes.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/python-net/working-with-tables/) documentation article.




**Inheritance:** [CellCollection](./) → [NodeCollection](../../aspose.words/nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Cell](../cell/) at the given index. |

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
|[ to_array()](./to_array/#default) | Copies all cells from the collection to a new array of cells. |

### Examples

Shows how to iterate through all tables in the document and print the contents of each cell.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
tables = doc.first_section.body.tables
self.assertEqual(2, len(list(tables)))
i = 0
while i < tables.count:
    print(f'Start of Table {i}')
    rows = tables[i].rows
    # We can use the "ToArray" method on a row collection to clone it into an array.
    self.assertSequenceEqual(list(rows), list(rows))
    self.assertNotEqual(rows, list(rows))
    j = 0
    while j < rows.count:
        print(f'\tStart of Row {j}')
        cells = rows[j].cells
        # We can use the "ToArray" method on a cell collection to clone it into an array.
        self.assertSequenceEqual(list(cells), list(cells))
        self.assertNotEqual(cells, list(cells))
        k = 0
        while k < cells.count:
            cell_text = cells[k].to_string(save_format=aw.SaveFormat.TEXT).strip()
            print(f'\t\tContents of Cell:{k} = "{cell_text}"')
            k += 1
        print(f'\tEnd of Row {j}')
        j += 1
    print(f'End of Table {i}\n')
    i += 1
```

### See Also

* module [aspose.words.tables](../)
* class [NodeCollection](../../aspose.words/nodecollection/)

