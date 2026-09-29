---
title: Font.engrave property
linktitle: engrave property
articleTitle: engrave property
second_title: Aspose.Words for Python
description: "Font.engrave property. True if the font is formatted as engraved."
type: docs
weight: 120
url: /tr/python-net/aspose.words/font/engrave/
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
# Aşağıda, metne 3D benzeri bir etki vermek için gölgeler kullanmanın iki yolu verilmiştir.
# 1 -  Metni oyma, harflerin sayfaya gömülmüş gibi görünmesini sağlar:
builder.font.engrave = True
builder.writeln('This text is engraved.')
# 2 -  Kabartma metin, harflerin sayfadan çıkıntı yapıyormuş gibi görünmesini sağlar:
builder.font.engrave = False
builder.font.emboss = True
builder.writeln('This text is embossed.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.EngraveEmboss.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

