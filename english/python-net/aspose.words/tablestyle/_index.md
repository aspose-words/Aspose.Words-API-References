---
title: TableStyle class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a table style."
type: docs
weight: 1170
url: /python-net/aspose.words/tablestyle/
---

## TableStyle class

Represents a table style.


**Inheritance:** [TableStyle](./) → [Style](../style/)

### Properties

| Name | Description |
| --- | --- |
| [aliases](../style/aliases/) | Gets all aliases of this style. If style has no aliases then empty array of string is returned.<br>(Inherited from [Style](../style/)) |
| [alignment](./alignment/) | Specifies the alignment for the table style. |
| [allow_break_across_pages](./allow_break_across_pages/) | Gets or sets a flag indicating whether text in a table row is allowed to split across a page break. |
| [base_style_name](../style/base_style_name/) | Gets/sets the name of the style this style is based on.<br>(Inherited from [Style](../style/)) |
| [bidi](./bidi/) | Gets or sets whether this is a style for a right-to-left table. |
| [borders](./borders/) | Gets the collection of default cell borders for the style. |
| [bottom_padding](./bottom_padding/) | Gets or sets the amount of space (in points) to add below the contents of table cells. |
| [built_in](../style/built_in/) | True if this style is one of the built-in styles in MS Word.<br>(Inherited from [Style](../style/)) |
| [cell_spacing](./cell_spacing/) | Gets or sets the amount of space (in points) between the cells. |
| [column_stripe](./column_stripe/) | Gets or sets a number of columns to include in the banding when the style specifies odd/even columns banding. |
| [conditional_styles](./conditional_styles/) | Collection of conditional styles that may be defined for this table style. |
| [document](../style/document/) | Gets the owner document.<br>(Inherited from [Style](../style/)) |
| [font](../style/font/) | Gets the character formatting of the style.<br>(Inherited from [Style](../style/)) |
| [is_heading](../style/is_heading/) | True when the style is one of the built-in Heading styles.<br>(Inherited from [Style](../style/)) |
| [is_quick_style](../style/is_quick_style/) | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.<br>(Inherited from [Style](../style/)) |
| [left_indent](./left_indent/) | Gets or sets the value that represents the left indent of a table. |
| [left_padding](./left_padding/) | Gets or sets the amount of space (in points) to add to the left of the contents of table cells. |
| [linked_style_name](../style/linked_style_name/) | Gets the name of the Style linked to this one. Returns Empty string if no styles are linked.<br>(Inherited from [Style](../style/)) |
| [list](../style/list/) | Gets the list that defines formatting of this list style.<br>(Inherited from [Style](../style/)) |
| [list_format](../style/list_format/) | Provides access to the list formatting properties of a paragraph style.<br>(Inherited from [Style](../style/)) |
| [name](../style/name/) | Gets or sets the name of the style.<br>(Inherited from [Style](../style/)) |
| [next_paragraph_style_name](../style/next_paragraph_style_name/) | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style.<br>(Inherited from [Style](../style/)) |
| [paragraph_format](../style/paragraph_format/) | Gets the paragraph formatting of the style.<br>(Inherited from [Style](../style/)) |
| [right_padding](./right_padding/) | Gets or sets the amount of space (in points) to add to the right of the contents of table cells. |
| [row_stripe](./row_stripe/) | Gets or sets a number of rows to include in the banding when the style specifies odd/even row banding. |
| [shading](./shading/) | Gets a [Shading](../shading/) object that refers to the shading formatting for table cells. |
| [style_identifier](../style/style_identifier/) | Gets the locale independent style identifier for a built-in style.<br>(Inherited from [Style](../style/)) |
| [styles](../style/styles/) | Gets the collection of styles this style belongs to.<br>(Inherited from [Style](../style/)) |
| [top_padding](./top_padding/) | Gets or sets the amount of space (in points) to add above the contents of table cells. |
| [type](../style/type/) | Gets the style type (paragraph or character).<br>(Inherited from [Style](../style/)) |
| [vertical_alignment](./vertical_alignment/) | Specifies the vertical alignment for the cells. |

### Methods

| Name | Description |
| --- | --- |
|[ equals(style)](../style/equals/#style) | Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared.<br>(Inherited from [Style](../style/)) |
|[ remove()](../style/remove/#default) | Removes the specified style from the document.<br>(Inherited from [Style](../style/)) |

### Examples

Shows how to create custom style settings for the table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("Name")
builder.insert_cell()
builder.write("مرحبًا")
builder.end_row()
builder.insert_cell()
builder.insert_cell()
builder.end_table()

table_style = doc.styles.add(aw.StyleType.TABLE, "MyTableStyle1").as_table_style()
table_style.allow_break_across_pages = True
table_style.bidi = True
table_style.cell_spacing = 5
table_style.bottom_padding = 20
table_style.left_padding = 5
table_style.right_padding = 10
table_style.top_padding = 20
table_style.shading.background_pattern_color = drawing.Color.antique_white
table_style.borders.color = drawing.Color.blue
table_style.borders.line_style = aw.LineStyle.DOT_DASH
table_style.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER

table.style = table_style

# Setting the style properties of a table may affect the properties of the table itself.
self.assertTrue(table.bidi)
self.assertEqual(5.0, table.cell_spacing)
self.assertEqual("MyTableStyle1", table.style_name)

doc.save(ARTIFACTS_DIR + "Table.table_style_creation.docx")
```

### See Also

* module [aspose.words](../)
* class [Style](../style/)

