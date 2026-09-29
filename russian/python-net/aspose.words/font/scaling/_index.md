---
title: Font.scaling property
linktitle: scaling property
articleTitle: scaling property
second_title: Aspose.Words for Python
description: "Font.scaling property. Gets or sets character width scaling in percent."
type: docs
weight: 320
url: /ru/python-net/aspose.words/font/scaling/
---

## Font.scaling property

Gets or sets character width scaling in percent.


```python
@property
def scaling(self) -> int:
    ...

@scaling.setter
def scaling(self, value: int):
    ...

```

### Examples

Shows how to set horizontal scaling and spacing for characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Добавьте пробег текста и увеличьте ширину символов до 150%.
builder.font.scaling = 150
builder.writeln('Wide characters')
# Добавьте пробег текста и добавьте 1pt дополнительного горизонтального интервала между каждым символом.
builder.font.spacing = 1
builder.writeln('Expanded by 1pt')
# Добавьте пробег текста и сблизьте символы друг с другом на 1pt.
builder.font.spacing = -1
builder.writeln('Condensed by 1pt')
doc.save(file_name=ARTIFACTS_DIR + 'Font.ScalingSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

