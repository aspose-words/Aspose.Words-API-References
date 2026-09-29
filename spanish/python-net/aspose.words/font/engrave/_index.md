---
title: Font.engrave property
linktitle: engrave property
articleTitle: engrave property
second_title: Aspose.Words for Python
description: "Font.engrave property. True if the font is formatted as engraved."
type: docs
weight: 120
url: /es/python-net/aspose.words/font/engrave/
---

## Font.engrave property

True if the font is formatted as engraved.


```python
@property
def engrave(self) -> bool:
    ...

@engrave.setter
def engrave(self, value: bool):
    ...

```

### Examples

Shows how to apply engraving/embossing effects to text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.size = 36
builder.font.color = aspose.pydrawing.Color.light_blue
# A continuación se presentan dos formas de usar sombras para aplicar un efecto similar a 3D al texto.
# 1 -  Grabar texto para que parezca que las letras están hundidas en la página:
builder.font.engrave = True
builder.writeln('This text is engraved.')
# 2 -  Relieve texto para que parezca que las letras sobresalen de la página:
builder.font.engrave = False
builder.font.emboss = True
builder.writeln('This text is embossed.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.EngraveEmboss.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

