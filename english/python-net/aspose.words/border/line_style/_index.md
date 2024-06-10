---
title: Border.line_style property
linktitle: line_style property
articleTitle: line_style property
second_title: Aspose.Words for Python
description: "Border.line_style property. Gets or sets the border style."
type: docs
weight: 40
url: /python-net/aspose.words/border/line_style/
---

## Border.line_style property

Gets or sets the border style.


```python
@property
def line_style(self) -> aspose.words.LineStyle:
    ...

@line_style.setter
def line_style(self, value: aspose.words.LineStyle):
    ...

```

### Remarks

If you set line style to none, then line width is automatically changed to zero.




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

### See Also

* module [aspose.words](../../)
* class [Border](../)

