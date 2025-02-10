---
title: Font.size property
linktitle: size property
articleTitle: size property
second_title: Aspose.Words for Python
description: "Font.size property. Gets or sets the font size in points."
type: docs
weight: 350
url: /python-net/aspose.words/font/size/
---

## Font.size property

Gets or sets the font size in points.


```python
@property
def size(self) -> float:
    ...

@size.setter
def size(self, value: float):
    ...

```

### Examples

Shows how to insert formatted text using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Specify font formatting, then add text.
font = builder.font
font.size = 16
font.bold = True
font.color = aspose.pydrawing.Color.blue
font.name = 'Courier New'
font.underline = aw.Underline.DASH
builder.write('Hello world!')
```

Shows how to format a run of text using its font property.

```python
doc = aw.Document()
run = aw.Run(doc=doc, text='Hello world!')
font = run.font
font.name = 'Courier New'
font.size = 36
font.highlight_color = aspose.pydrawing.Color.yellow
doc.first_section.body.first_paragraph.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.CreateFormattedRun.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

