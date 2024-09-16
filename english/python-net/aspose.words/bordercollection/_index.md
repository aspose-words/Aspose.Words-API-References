---
title: BorderCollection class
linktitle: BorderCollection class
articleTitle: BorderCollection class
second_title: Aspose.Words for Python
description: "aspose.words.BorderCollection class. A collection of [Border](../border/) objects"
type: docs
weight: 90
url: /python-net/aspose.words/bordercollection/
---

## BorderCollection class

A collection of [Border](../border/) objects.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




### Remarks

Different document elements have different borders.
For example, [ParagraphFormat](../paragraphformat/) has [BorderCollection.bottom](./bottom/), [BorderCollection.left](./left/), [BorderCollection.right](./right/) and [BorderCollection.top](./top/) borders.
You can specify different formatting for each border independently or
enumerate through all borders and apply same formatting.



### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Border](../border/) object by index. |

### Properties

| Name | Description |
| --- | --- |
| [bottom](./bottom/) | Gets the bottom border. |
| [color](./color/) | Gets or sets the border color. |
| [count](./count/) | Gets the number of borders in the collection. |
| [distance_from_text](./distance_from_text/) | Gets or sets distance of the border from text in points. |
| [horizontal](./horizontal/) | Gets the horizontal border that is used between cells or conforming paragraphs. |
| [left](./left/) | Gets the left border. |
| [line_style](./line_style/) | Gets or sets the border style. |
| [line_width](./line_width/) | Gets or sets the border width in points. |
| [right](./right/) | Gets the right border. |
| [shadow](./shadow/) | Gets or sets a value indicating whether the border has a shadow. |
| [top](./top/) | Gets the top border. |
| [vertical](./vertical/) | Gets the vertical border that is used between cells. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Removes all borders of an object. |
|[ equals(br_coll)](./equals/#bordercollection) | Compares collections of borders. |
|[ get_by_border_type(border_type)](./get_by_border_type/#bordertype) | Retrieves a [Border](../border/) object by border type. |

### Examples

Shows how to insert a paragraph with a top border.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
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

