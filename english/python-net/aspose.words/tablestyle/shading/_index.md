﻿---
title: TableStyle.shading property
linktitle: shading property
articleTitle: shading property
second_title: Aspose.Words for Python
description: "TableStyle.shading property. Gets a [Shading](../../shading/) object that refers to the shading formatting for table cells."
type: docs
weight: 130
url: /python-net/aspose.words/tablestyle/shading/
---

## TableStyle.shading property

Gets a [Shading](../../shading/) object that refers to the shading formatting for table cells.



```python
@property
def shading(self) -> aspose.words.Shading:
    ...

```

### Examples

Shows how to create custom style settings for the table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Name')
builder.insert_cell()
builder.write('مرحبًا')
builder.end_row()
builder.insert_cell()
builder.insert_cell()
builder.end_table()
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
table_style.allow_break_across_pages = True
table_style.bidi = True
table_style.cell_spacing = 5
table_style.bottom_padding = 20
table_style.left_padding = 5
table_style.right_padding = 10
table_style.top_padding = 20
table_style.shading.background_pattern_color = aspose.pydrawing.Color.antique_white
table_style.borders.color = aspose.pydrawing.Color.blue
table_style.borders.line_style = aw.LineStyle.DOT_DASH
table_style.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
table.style = table_style
# Setting the style properties of a table may affect the properties of the table itself.
self.assertTrue(table.bidi)
self.assertEqual(5, table.cell_spacing)
self.assertEqual('MyTableStyle1', table.style_name)
doc.save(file_name=ARTIFACTS_DIR + 'Table.TableStyleCreation.docx')
```

### See Also

* module [aspose.words](../../)
* class [TableStyle](../)

