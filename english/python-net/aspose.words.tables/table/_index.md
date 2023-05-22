﻿---
title: Table class
linktitle: Table class
articleTitle: Table class
second_title: Aspose.Words for Python
description: "aspose.words.tables.Table class. Represents a table in a Word document"
type: docs
weight: 120
url: /python-net/aspose.words.tables/table/
---

## Table class

Represents a table in a Word document.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/python-net/working-with-tables/) documentation article.




[Table](./) is a block-level node and can be a child of classes derived from [Story](../../aspose.words/story/) or
[InlineStory](../../aspose.words/inlinestory/).

[Table](./) can contain one or more [Row](../row/) nodes.

A minimal valid table needs to have at least one [Row](../row/).




**Inheritance:** [Table](./) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [Table(doc)](./__init__/#documentbase) | Initializes a new instance of the [Table](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [absolute_horizontal_distance](./absolute_horizontal_distance/) | Gets or sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0. |
| [absolute_vertical_distance](./absolute_vertical_distance/) | Gets or sets absolute vertical floating table position specified by the table properties, in points. Default value is 0. |
| [alignment](./alignment/) | Specifies how an inline table is aligned in the document. |
| [allow_auto_fit](./allow_auto_fit/) | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [allow_cell_spacing](./allow_cell_spacing/) | Gets or sets the "Allow spacing between cells" option. |
| [allow_overlap](./allow_overlap/) | Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is ``True``. |
| [bidi](./bidi/) | Gets or sets whether this is a right-to-left table. |
| [bottom_padding](./bottom_padding/) | Gets or sets the amount of space (in points) to add below the contents of cells. |
| [cell_spacing](./cell_spacing/) | Gets or sets the amount of space (in points) between the cells. |
| [child_nodes](../../aspose.words/compositenode/child_nodes/) | Gets all immediate child nodes of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [description](./description/) | Gets or sets description of this table. It provides an alternative text representation of the information contained in the table. |
| [distance_bottom](./distance_bottom/) | Gets or sets distance between table bottom and the surrounding text, in points. |
| [distance_left](./distance_left/) | Gets or sets distance between table left and the surrounding text, in points. |
| [distance_right](./distance_right/) | Gets or sets distance between table right and the surrounding text, in points. |
| [distance_top](./distance_top/) | Gets or sets distance between table top and the surrounding text, in points. |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [first_row](./first_row/) | Returns the first [Row](../row/) node in the table. |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [horizontal_anchor](./horizontal_anchor/) | Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [RelativeHorizontalPosition.COLUMN](../../aspose.words.drawing/relativehorizontalposition/#COLUMN). |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [last_row](./last_row/) | Returns the last [Row](../row/) node in the table. |
| [left_indent](./left_indent/) | Gets or sets the value that represents the left indent of the table. |
| [left_padding](./left_padding/) | Gets or sets the amount of space (in points) to add to the left of the contents of cells. |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.TABLE](../../aspose.words/nodetype/#TABLE). |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [preferred_width](./preferred_width/) | Gets or sets the table preferred width. |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [relative_horizontal_alignment](./relative_horizontal_alignment/) | Gets or sets floating table relative horizontal alignment. |
| [relative_vertical_alignment](./relative_vertical_alignment/) | Gets or sets floating table relative vertical alignment. |
| [right_padding](./right_padding/) | Gets or sets the amount of space (in points) to add to the right of the contents of cells. |
| [rows](./rows/) | Provides typed access to the rows of the table. |
| [style](./style/) | Gets or sets the table style applied to this table. |
| [style_identifier](./style_identifier/) | Gets or sets the locale independent style identifier of the table style applied to this table. |
| [style_name](./style_name/) | Gets or sets the name of the table style applied to this table. |
| [style_options](./style_options/) | Gets or sets bit flags that specify how a table style is applied to this table. |
| [text_wrapping](./text_wrapping/) | Gets or sets [Table.text_wrapping](./text_wrapping/) for table. |
| [title](./title/) | Gets or sets title of this table. It provides an alternative text representation of the information contained in the table. |
| [top_padding](./top_padding/) | Gets or sets the amount of space (in points) to add above the contents of cells. |
| [vertical_anchor](./vertical_anchor/) | Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [RelativeVerticalPosition.MARGIN](../../aspose.words.drawing/relativeverticalposition/#MARGIN). |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ auto_fit(behavior)](./auto_fit/#autofitbehavior) | Resizes the table and cells according to the specified auto fit behavior. |
|[ clear_borders()](./clear_borders/#default) | Removes all table and cell borders on this table. |
|[ clear_shading()](./clear_shading/#default) | Removes all shading on the table. |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ convert_to_horizontally_merged_cells()](./convert_to_horizontally_merged_cells/#default) | Converts cells horizontally merged by width to cells merged by [CellFormat.horizontal_merge](../cellformat/horizontal_merge/). |
|[ ensure_minimum()](./ensure_minimum/#default) | If the table has no rows, creates and appends one [Row](../row/). |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#unknown) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_child(node_type, index, is_deep)](../../aspose.words/compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../../aspose.words/compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
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
|[ set_border(border_type, line_style, line_width, color, is_override_cell_borders)](./set_border/#bordertype_linestyle_float_color_bool) | Sets the specified table border to the specified line style, width and color. |
|[ set_borders(line_style, line_width, color)](./set_borders/#linestyle_float_color) | Sets all table borders to the specified line style, width and color. |
|[ set_shading(texture, foreground_color, background_color)](./set_shading/#textureindex_color_color) | Sets shading to the specified values on whole table. |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to build a formatted 2x2 table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.write("Row 1, cell 1.")
builder.insert_cell()
builder.write("Row 1, cell 2.")
builder.end_row()

# While building the table, the document builder will apply its current row_format/cell_format property values
# to the current row/cell that its cursor is in and any new rows/cells as it creates them.
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[0].cell_format.vertical_alignment)
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[1].cell_format.vertical_alignment)

builder.insert_cell()
builder.row_format.height = 100
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write("Row 2, cell 1.")
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write("Row 2, cell 2.")
builder.end_row()
builder.end_table()

# Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
self.assertEqual(aw.TextOrientation.UPWARD, table.rows[1].cells[0].cell_format.orientation)
self.assertEqual(aw.TextOrientation.DOWNWARD, table.rows[1].cells[1].cell_format.orientation)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.build_table.docx")
```

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

