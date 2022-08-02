---
title: count property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the number of nodes in the collection."
type: docs
weight: 20
url: /python-net/aspose.words/nodecollection/count/
---

## NodeCollection.count property

Gets the number of nodes in the collection.


### Examples

Shows how to traverse through a composite node's collection of child nodes.

```python
doc = aw.Document()

# Add two runs and one shape as child nodes to the first paragraph of this document.
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
paragraph.append_child(aw.Run(doc, "Hello world! "))

shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
# Note that the 'custom_node_id' is not saved to an output file and exists only during the node lifetime.
shape.custom_node_id = 100
shape.wrap_type = aw.drawing.WrapType.INLINE
paragraph.append_child(shape)

paragraph.append_child(aw.Run(doc, "Hello again!"))

# Iterate through the paragraph's collection of immediate children,
# and print any runs or shapes that we find within.
children = paragraph.child_nodes

self.assertEqual(3, paragraph.child_nodes.count)

for child in children:
    if child.node_type == aw.NodeType.RUN:
        print("Run contents:")
        print(f"\t\"{child.get_text().strip()}\"")

    elif child.node_type == aw.NodeType.SHAPE:
        child_shape = child.as_shape()
        print("Shape:")
        print(f"\t{child_shape.shape_type}, {child_shape.width}x{child_shape.height}")
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

* module [aspose.words](../../)
* class [NodeCollection](../)

