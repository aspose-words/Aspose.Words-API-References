---
title: Font.emboss property
linktitle: emboss property
articleTitle: emboss property
second_title: Aspose.Words for Python
description: "Font.emboss property. True if the font is formatted as embossed."
type: docs
weight: 100
url: /fr/python-net/aspose.words/font/emboss/
---

## Font.emboss property

True if the font is formatted as embossed.


```python
@property
def emboss(self) -> bool:
    ...

@emboss.setter
def emboss(self, value: bool):
    ...

```

### Examples

Shows how to apply engraving/embossing effects to text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.size = 36
builder.font.color = aspose.pydrawing.Color.light_blue
# Voici deux façons d'utiliser les ombres pour appliquer un effet 3D au texte.
# 1 -  Graver le texte pour donner l'impression que les lettres sont enfoncées dans la page :
builder.font.engrave = True
builder.writeln('This text is engraved.')
# 2 -  Embosser le texte pour donner l'impression que les lettres ressortent de la page :
builder.font.engrave = False
builder.font.emboss = True
builder.writeln('This text is embossed.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.EngraveEmboss.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

