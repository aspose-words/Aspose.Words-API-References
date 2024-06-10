---
title: Table.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "Table.node_type property. Returns [NodeType.TABLE](../../../aspose.words/nodetype/#TABLE)."
type: docs
weight: 210
url: /python-net/aspose.words.tables/table/node_type/
---

## Table.node_type property

Returns [NodeType.TABLE](../../../aspose.words/nodetype/#TABLE).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to find out if a tables are nested.

```python
def calculate_depth_of_nested_tables():
    doc = aw.Document(MY_DIR + 'Nested tables.docx')
    tables = doc.get_child_nodes(aw.NodeType.TABLE, True)
    for i in range(tables.count):
        table = tables[i].as_table()
        # Find out if any cells in the table have other tables as children.
        count = get_child_table_count(table)
        print(f'Table #{i} has {count} tables directly within its cells')
        # Find out if the table is nested inside another table, and, if so, at what depth.
        table_depth = get_nested_depth_of_table(table)
        if table_depth > 0:
            print(f'Table #{i} is nested inside another table at depth of {table_depth}')
        else:
            print('Table #{i} is a non nested table (is not a child of another table)')

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

* module [aspose.words.tables](../../)
* class [Table](../)

