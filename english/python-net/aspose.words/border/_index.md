---
title: Border class
linktitle: Border class
articleTitle: Border class
second_title: Aspose.Words for Python
description: "aspose.words.Border class. Represents a border of an object"
type: docs
weight: 80
url: /python-net/aspose.words/border/
---

## Border class

Represents a border of an object.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




### Remarks

Borders can be applied to various document elements including paragraph,
run of text inside a paragraph or a table cell.




**Inheritance:** [Border](./) → [InternableComplexAttr](../internablecomplexattr/)

### Properties

| Name | Description |
| --- | --- |
| [color](./color/) | Gets or sets the border color. |
| [distance_from_text](./distance_from_text/) | Gets or sets distance of the border from text or from the page edge in points. |
| [is_visible](./is_visible/) | Returns ``True`` if the [Border.line_style](./line_style/) is not [LineStyle.NONE](../linestyle/#NONE). |
| [line_style](./line_style/) | Gets or sets the border style. |
| [line_width](./line_width/) | Gets or sets the border width in points. |
| [shadow](./shadow/) | Gets or sets a value indicating whether the border has a shadow. |
| [theme_color](./theme_color/) | Gets or sets the theme color in the applied color scheme that is associated with this Border object. |
| [tint_and_shade](./tint_and_shade/) | Gets or sets a double value that lightens or darkens a color. |

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
builder.font.border.color = aspose.pydrawing.Color.green
builder.font.border.line_width = 2.5
builder.font.border.line_style = aw.LineStyle.DASH_DOT_STROKER
builder.write('Text surrounded by green border.')
doc.save(file_name=ARTIFACTS_DIR + 'Border.FontBorder.docx')
```

Shows how to insert a paragraph with a top border.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
top_border = builder.paragraph_format.borders.top
top_border.line_width = 4
top_border.line_style = aw.LineStyle.DASH_SMALL_GAP
# Set ThemeColor only when LineWidth or LineStyle setted.
top_border.theme_color = aw.themes.ThemeColor.ACCENT1
top_border.tint_and_shade = 0.25
builder.writeln('Text with a top border.')
doc.save(file_name=ARTIFACTS_DIR + 'Border.ParagraphTopBorder.docx')
```

### See Also

* module [aspose.words](../)
* class [InternableComplexAttr](../internablecomplexattr/)

