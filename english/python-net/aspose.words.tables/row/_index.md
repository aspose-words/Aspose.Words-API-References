---
title: Row class
linktitle: Row class
articleTitle: Row class
second_title: Aspose.Words for Python
description: "aspose.words.tables.Row class. Represents a table row"
type: docs
weight: 90
url: /python-net/aspose.words.tables/row/
---

## Row class

Represents a table row.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/python-net/working-with-tables/) documentation article.




### Remarks

[Row](./) can only be a child of a [Table](../table/).

[Row](./) can contain one or more [Cell](../cell/) nodes.

A minimal valid row needs to have at least one [Cell](../cell/).




**Inheritance:** [Row](./) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [Row(doc)](./__init__/#documentbase) | Initializes a new instance of the [Row](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [cells](./cells/) | Provides typed access to the [Cell](../cell/) child nodes of the row. |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [first_cell](./first_cell/) | Returns the first [Cell](../cell/) in the row. |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [is_first_row](./is_first_row/) | True if this is the first row in a table; false otherwise. |
| [is_last_row](./is_last_row/) | True if this is the last row in a table; false otherwise. |
| [last_cell](./last_cell/) | Returns the last [Cell](../cell/) in the row. |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [next_row](./next_row/) | Gets the next [Row](./) node. |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.ROW](../../aspose.words/nodetype/#ROW). |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parent_table](./parent_table/) | Returns the immediate parent table of the row. |
| [previous_row](./previous_row/) | Gets the previous [Row](./) node. |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [row_format](./row_format/) | Provides access to the formatting properties of the row. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ accept_end(visitor)](../../aspose.words/compositenode/accept_end/#documentvisitor) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ accept_start(visitor)](../../aspose.words/compositenode/accept_start/#documentvisitor) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ ensure_minimum()](./ensure_minimum/#default) | If the [Row](./) has no cells, creates and appends one [Cell](../cell/). |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_child(node_type, index, is_deep)](../../aspose.words/compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../../aspose.words/compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_text()](./get_text/#default) | Gets the text of all cells in this row including the end of row character. |
|[ index_of(child)](../../aspose.words/compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_after(new_child, ref_child)](../../aspose.words/compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_before(new_child, ref_child)](../../aspose.words/compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ prepend_child(new_child)](../../aspose.words/compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove_all_children()](../../aspose.words/compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_child(old_child)](../../aspose.words/compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_smart_tags()](../../aspose.words/compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_nodes(xpath)](../../aspose.words/compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_single_node(xpath)](../../aspose.words/compositenode/select_single_node/#str) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to create a table.

```python
doc = aw.Document()
table = aw.tables.Table(doc)
doc.first_section.body.append_child(table)

# Tables contain rows, which contain cells, which may have paragraphs
# with typical elements such as runs, shapes, and even other tables.
# Calling the "ensure_minimum" method on a table will ensure that
# the table has at least one row, cell, and paragraph.
first_row = aw.tables.Row(doc)
table.append_child(first_row)

first_cell = aw.tables.Cell(doc)
first_row.append_child(first_cell)

paragraph = aw.Paragraph(doc)
first_cell.append_child(paragraph)

# Add text to the first cell in the first row of the table.
run = aw.Run(doc, "Hello world!")
paragraph.append_child(run)

doc.save(ARTIFACTS_DIR + "Table.create_table.docx")
```

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

Shows how to build a nested table without using a document builder.

```python
def test_create_nested_table(self):

    doc = aw.Document()

    # Create the outer table with three rows and four columns, and then add it to the document.
    outer_table = ExTable.create_table(doc, 3, 4, "Outer Table")
    doc.first_section.body.append_child(outer_table)

    # Create another table with two rows and two columns and then insert it into the first table's first cell.
    inner_table = ExTable.create_table(doc, 2, 2, "Inner Table")
    outer_table.first_row.first_cell.append_child(inner_table)

    doc.save(ARTIFACTS_DIR + "Table.create_nested_table.docx")

@staticmethod
def create_table(doc: aw.Document, row_count: int, cell_count: int, cell_text: str) -> aw.tables.Table:
    """Creates a new table in the document with the given dimensions and text in each cell."""
    table = aw.tables.Table(doc)

    for row_id in range(1, row_count + 1):
        row = aw.tables.Row(doc)
        table.append_child(row)

        for cell_id in range(1, cell_count + 1):
            cell = aw.tables.Cell(doc)
            cell.append_child(aw.Paragraph(doc))
            cell.first_paragraph.append_child(aw.Run(doc, cell_text))

            row.append_child(cell)

    # You can use the "title" and "description" properties to add a title and description respectively to your table.
    # The table must have at least one row before we can use these properties.
    # These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
    # If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
    table.title = "Aspose table title"
    table.description = "Aspose table description"

    return table
```

### See Also

* module [aspose.words.tables](../)
* class [CompositeNode](../../aspose.words/compositenode/)

