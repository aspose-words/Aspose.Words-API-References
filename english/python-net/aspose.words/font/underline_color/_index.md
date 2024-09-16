---
title: Font.underline_color property
linktitle: underline_color property
articleTitle: underline_color property
second_title: Aspose.Words for Python
description: "Font.underline_color property. Gets or sets the color of the underline applied to the font."
type: docs
weight: 540
url: /python-net/aspose.words/font/underline_color/
---

## Font.underline_color property

Gets or sets the color of the underline applied to the font.


```python
@property
def underline_color(self) -> aspose.pydrawing.Color:
    ...

@underline_color.setter
def underline_color(self, value: aspose.pydrawing.Color):
    ...

```

### Examples

Shows how to configure the style and color of a text underline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.underline = aw.Underline.DOTTED
builder.font.underline_color = aspose.pydrawing.Color.red
builder.writeln('Underlined text.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Underlines.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

