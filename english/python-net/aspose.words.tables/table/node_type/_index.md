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

Shows how to traverse a composite node's tree of child nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Any node that can contain child nodes, such as the document itself, is composite.
self.assertTrue(doc.is_composite)
# Invoke the recursive function that will go through and print all the child nodes of a composite node.
self.traverse_all_nodes(doc, 0)
```

Shows how to traverse a composite node's tree of child nodes (TraverseAllNodes).

```python
def traverse_all_nodes(self, parent_node, depth):
    child_node = parent_node.first_child
    while child_node != None:
        sys.stdout.write(f'\t' * depth + aw.Node.node_type_to_string(child_node.node_type))
        # Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
        if child_node.is_composite:
            sys.stdout.write('\n')
            self.traverse_all_nodes(child_node.as_composite_node(), depth + 1)
        elif isinstance(child_node, aw.Inline):
            sys.stdout.write(f' - "{child_node.get_text().strip()}"\n')
        else:
            sys.stdout.write('\n')
        child_node = child_node.next_sibling
```

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
* class [Table](../)

