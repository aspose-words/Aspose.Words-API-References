---
title: Shading class
second_title: Aspose.Words for Python via .NET API Reference
description: "Contains shading attributes for an object"
type: docs
weight: 1030
url: /python-net/aspose.words/shading/
---

## Shading class

Contains shading attributes for an object.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.




**Inheritance:** [Shading](./) → [InternableComplexAttr](../internablecomplexattr/)

### Properties

| Name | Description |
| --- | --- |
| [background_pattern_color](./background_pattern_color/) | Gets or sets the color that's applied to the background of the [Shading](./) object. |
| [foreground_pattern_color](./foreground_pattern_color/) | Gets or sets the color that's applied to the foreground of the [Shading](./) object. |
| [texture](./texture/) | Gets or sets the shading texture. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Removes shading from the object. |
|[ equals(rhs)](./equals/#shading) | Determines whether the specified [Shading](./) is equal in value to the current [Shading](./). |

### Examples

Shows how to apply border and shading color while building a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Start a table and set a default color/thickness for its borders.
table = builder.start_table()
table.set_borders(aw.LineStyle.SINGLE, 2.0, drawing.Color.black)

# Create a row with two cells with different background colors.
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = drawing.Color.light_sky_blue
builder.writeln("Row 1, Cell 1.")
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = drawing.Color.orange
builder.writeln("Row 1, Cell 2.")
builder.end_row()

# Reset cell formatting to disable the background colors
# set a custom border thickness for all new cells created by the builder,
# then build a second row.
builder.cell_format.clear_formatting()
builder.cell_format.borders.left.line_width = 4.0
builder.cell_format.borders.right.line_width = 4.0
builder.cell_format.borders.top.line_width = 4.0
builder.cell_format.borders.bottom.line_width = 4.0

builder.insert_cell()
builder.writeln("Row 2, Cell 1.")
builder.insert_cell()
builder.writeln("Row 2, Cell 2.")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.table_borders_and_shading.docx")
```

Shows how to decorate text with borders and shading.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

borders = builder.paragraph_format.borders
borders.distance_from_text = 20
borders.left.line_style = aw.LineStyle.DOUBLE
borders.right.line_style = aw.LineStyle.DOUBLE
borders.top.line_style = aw.LineStyle.DOUBLE
borders.bottom.line_style = aw.LineStyle.DOUBLE

shading = builder.paragraph_format.shading
shading.texture = aw.TextureIndex.TEXTURE_DIAGONAL_CROSS
shading.background_pattern_color = drawing.Color.light_coral
shading.foreground_pattern_color = drawing.Color.light_salmon

builder.write("This paragraph is formatted with a double border and shading.")
doc.save(ARTIFACTS_DIR + "DocumentBuilder.apply_borders_and_shading.docx")
```

### See Also

* module [aspose.words](../)
* class [InternableComplexAttr](../internablecomplexattr/)

