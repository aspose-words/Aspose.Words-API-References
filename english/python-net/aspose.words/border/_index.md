---
title: Border class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a border of an object."
type: docs
weight: 70
url: /python-net/aspose.words/border/
---

## Border class

Represents a border of an object.


Borders can be applied to various document elements including paragraph,
run of text inside a paragraph or a table cell.




**Inheritance:** [Border](./) → [InternableComplexAttr](../internablecomplexattr/)

### Properties

| Name | Description |
| --- | --- |
| [color](./color/) | Gets or sets the border color. |
| [distance_from_text](./distance_from_text/) | Gets or sets distance of the border from text or from the page edge in points. |
| [is_visible](./is_visible/) | Returns true if the LineStyle is not LineStyle.None. |
| [line_style](./line_style/) | Gets or sets the border style. |
| [line_width](./line_width/) | Gets or sets the border width in points. |
| [shadow](./shadow/) | Gets or sets a value indicating whether the border has a shadow. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Resets border properties to default values. |
|[ equals(rhs)](./equals/#border) | Determines whether the specified border is equal in value to the current border. |

### Examples

Shows how to insert a string surrounded by a border into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.border.color = drawing.Color.green
builder.font.border.line_width = 2.5
builder.font.border.line_style = aw.LineStyle.DASH_DOT_STROKER

builder.write("Text surrounded by green border.")

doc.save(ARTIFACTS_DIR + "Border.font_border.docx")
```

Shows how to insert a paragraph with a top border.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

top_border = builder.paragraph_format.borders.top
top_border.color = drawing.Color.red
top_border.line_width = 4.0
top_border.line_style = aw.LineStyle.DASH_SMALL_GAP

builder.writeln("Text with a red top border.")

doc.save(ARTIFACTS_DIR + "Border.paragraph_top_border.docx")
```

### See Also

* module [aspose.words](../)
* class [InternableComplexAttr](../internablecomplexattr/)

