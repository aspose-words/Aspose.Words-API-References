---
title: BorderType enumeration
linktitle: BorderType enumeration
articleTitle: BorderType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.BorderType enumeration. Specifies sides of a border"
type: docs
weight: 110
url: /python-net/aspose.words/bordertype/
---

## BorderType enumeration

Specifies sides of a border.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




### Members

| Name | Description |
| --- | --- |
| NONE | Default value. |
| BOTTOM | Specifies the bottom border of a paragraph or a table cell. |
| LEFT | Specifies the left border of a paragraph or a table cell. |
| RIGHT | Specifies the right border of a paragraph or a table cell. |
| TOP | Specifies the top border of a paragraph or a table cell. |
| HORIZONTAL | Specifies the horizontal border between cells in a table or between conforming paragraphs. |
| VERTICAL | Specifies the vertical border between cells in a table. |
| DIAGONAL_DOWN | Specifies the diagonal border in a table cell. |
| DIAGONAL_UP | Specifies the diagonal border in a table cell. |

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

