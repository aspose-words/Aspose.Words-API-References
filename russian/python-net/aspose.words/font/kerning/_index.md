---
title: Font.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for Python
description: "Font.kerning property. Gets or sets the font size at which kerning starts."
type: docs
weight: 180
url: /ru/python-net/aspose.words/font/kerning/
---

## Font.kerning property

Gets or sets the font size at which kerning starts.


```python
@property
def kerning(self) -> float:
    ...

@kerning.setter
def kerning(self, value: float):
    ...

```

### Examples

Shows how to specify the font size at which kerning begins to take effect.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial Black'
# Установите размер шрифта конструктора и минимальный размер, при котором будет применяться кернинг.
# Размер шрифта опускается ниже порога кернинга, поэтому пробег ниже не будет иметь кернинга.
builder.font.size = 18
builder.font.kerning = 24
builder.writeln('TALLY. (Kerning not applied)')
# Установите порог кернинга так, чтобы текущий размер шрифта конструктора был выше его.
# Любой текст, который мы добавим с этого момента, будет иметь примененный кернинг. Пробелы между символами
# будут скорректированы, обычно в результате чего пробег текста будет немного более эстетичным.
builder.font.kerning = 12
builder.writeln('TALLY. (Kerning applied)')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Kerning.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

