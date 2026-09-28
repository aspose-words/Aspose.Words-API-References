---
title: Font.outline property
linktitle: outline property
articleTitle: outline property
second_title: Aspose.Words for Python
description: "Font.outline property. True if the font is formatted as outline."
type: docs
weight: 300
url: /ar/python-net/aspose.words/font/outline/
---

## Font.outline property

True if the font is formatted as outline.


```python
@property
def outline(self) -> bool:
    ...

@outline.setter
def outline(self, value: bool):
    ...

```

### Examples

Shows how to create a run of text formatted as outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# عيّن علامة Outline لتغيير لون تعبئة النص إلى الأبيض و
# اترك حدًا رفيعًا حول كل حرف بلون النص الأصلي.
builder.font.outline = True
builder.font.color = aspose.pydrawing.Color.blue
builder.font.size = 36
builder.writeln('This text has an outline.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Outline.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

