---
title: Cell.tables property
linktitle: tables property
articleTitle: tables property
second_title: Aspose.Words for Python
description: "Cell.tables property. Gets a collection of tables that are immediate children of the cell."
type: docs
weight: 120
url: /python-net/aspose.words.tables/cell/tables/
---

## Cell.tables property

Gets a collection of tables that are immediate children of the cell.


```python
@property
def tables(self) -> aspose.words.tables.TableCollection:
    ...

```

### Examples

Shows how to find out if a tables are nested.

```python
doc = aw.Document(file_name=MY_DIR + 'Nested tables.docx')
tables = doc.get_child_nodes(aw.NodeType.TABLE, True)
i = 0
while i < tables.count:
    table = tables[i].as_table()
    # Find out if any cells in the table have other tables as children.
    count = ExTable._get_child_table_count(table)
    print('Table #{0} has {1} tables directly within its cells'.format(i, count))
    # Find out if the table is nested inside another table, and, if so, at what depth.
    table_depth = ExTable._get_nested_depth_of_table(table)
    if table_depth > 0:
        print('Table #{0} is nested inside another table at depth of {1}'.format(i, table_depth))
    else:
        print('Table #{0} is a non nested table (is not a child of another table)'.format(i))
    i += 1
```

Shows how to find out if a tables are nested (GetNestedDepthOfTable).

```python
@staticmethod
def _get_nested_depth_of_table(table):
    depth = 0
    parent = table.get_ancestor(aw.tables.Table)
    while parent is not None:
        depth += 1
        parent = parent.get_ancestor(aw.tables.Table)
    return depth

@staticmethod
def _get_child_table_count(table):
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
* class [Cell](../)

