---
title: Table.set_border method
linktitle: set_border method
articleTitle: set_border method
second_title: Aspose.Words for Python
description: "Table.set_border method. Sets the specified table border to the specified line style, width and color."
type: docs
weight: 410
url: /python-net/aspose.words.tables/table/set_border/
---

## set_border(border_type, line_style, line_width, color, is_override_cell_borders) {#bordertype_linestyle_float_color_bool}

Sets the specified table border to the specified line style, width and color.


```python
def set_border(self, border_type: aspose.words.BorderType, line_style: aspose.words.LineStyle, line_width: float, color: aspose.pydrawing.Color, is_override_cell_borders: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| border_type | [BorderType](../../../aspose.words/bordertype/) |  |
| line_style | [LineStyle](../../../aspose.words/linestyle/) |  |
| line_width | float |  |
| color | aspose.pydrawing.Color |  |
| is_override_cell_borders | bool |  |

### Examples

Shows how to apply an outline border to a table.

```python
doc = aw.Document(MY_DIR + "Tables.docx")
table = doc.first_section.body.tables[0]

# Align the table to the center of the page.
table.alignment = aw.tables.TableAlignment.CENTER

# Clear any existing borders and shading from the table.
table.clear_borders()
table.clear_shading()

# Add green borders to the outline of the table.
table.set_border(aw.BorderType.LEFT, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)
table.set_border(aw.BorderType.RIGHT, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)
table.set_border(aw.BorderType.TOP, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)
table.set_border(aw.BorderType.BOTTOM, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)

# Fill the cells with a light green solid color.
table.set_shading(aw.TextureIndex.TEXTURE_SOLID, drawing.Color.light_green, drawing.Color.empty())

doc.save(ARTIFACTS_DIR + "Table.set_outline_borders.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

