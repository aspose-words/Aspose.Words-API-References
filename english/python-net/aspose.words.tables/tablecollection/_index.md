---
title: TableCollection class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides typed access to a collection of [Table](../table/) nodes"
type: docs
weight: 140
url: /python-net/aspose.words.tables/tablecollection/
---

## TableCollection class

Provides typed access to a collection of [Table](../table/) nodes.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/net/working-with-tables/) documentation article.




**Inheritance:** [TableCollection](./) → [NodeCollection](../../aspose.words/nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Table](../table/) at the given index. |

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
|[ to_array()](./to_array/#default) | Copies all tables from the collection to a new array of tables. |

### Examples

Shows how to remove the first and last rows of all tables in a document.

```python
doc = aw.Document(MY_DIR + "Tables.docx")

tables = doc.first_section.body.tables

self.assertEqual(5, tables[0].rows.count)
self.assertEqual(4, tables[1].rows.count)

for table in tables:
    table = table.as_table()

    if table.first_row is not None:
        table.first_row.remove()

    if table.last_row is not None:
        table.last_row.remove()

self.assertEqual(3, tables[0].rows.count)
self.assertEqual(2, tables[1].rows.count)
```

Shows how to find out if a tables are nested.

```python
def test_calculate_depth_of_nested_tables(self):

    doc = aw.Document(MY_DIR + "Nested tables.docx")
    tables = doc.get_child_nodes(aw.NodeType.TABLE, True)

    for i in range(tables.count):
        table = tables[i].as_table()

        # Find out if any cells in the table have other tables as children.
        count = self.get_child_table_count(table)
        print(f"Table #{i} has {count} tables directly within its cells")

        # Find out if the table is nested inside another table, and, if so, at what depth.
        table_depth = self.get_nested_depth_of_table(table)

        if table_depth > 0:
            print(f"Table #{i} is nested inside another table at depth of {table_depth}")
        else:
            print("Table #{i} is a non nested table (is not a child of another table)")

@staticmethod
def get_nested_depth_of_table(table: aw.tables.Table) -> int:
    """Calculates what level a table is nested inside other tables.

    :return: An integer indicating the nesting depth of the table (number of parent table nodes).
    """

    depth = 0
    parent = table.get_ancestor(table.node_type)

    while parent is not None:
        depth += 1
        parent = parent.get_ancestor(table.node_type)

    return depth

@staticmethod
def get_child_table_count(table: aw.tables.Table) -> int:
    """Determines if a table contains any immediate child table within its cells.

    Do not recursively traverse through those tables to check for further tables.

    :return: Returns True if at least one child cell contains a table.
             Returns False if no cells in the table contain a table.
    """

    child_table_count = 0

    for row in table.rows:
        row = row.as_row()

        for cell in row.cells:
            cell = cell.as_cell()

            child_tables = cell.tables

            if child_tables.count > 0:
                child_table_count += 1

    return child_table_count
```

### See Also

* module [aspose.words.tables](../)
* class [NodeCollection](../../aspose.words/nodecollection/)

