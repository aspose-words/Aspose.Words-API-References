---
title: Font.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for Python
description: "Font.kerning property. Gets or sets the font size at which kerning starts."
type: docs
weight: 180
url: /fr/python-net/aspose.words/font/kerning/
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
# Définissez la taille de police du générateur, ainsi que la taille minimale à laquelle le crénage prendra effet.
# La taille de police tombe en dessous du seuil de crénage, donc l'exécution ci-dessous n'aura pas de crénage.
builder.font.size = 18
builder.font.kerning = 24
builder.writeln('TALLY. (Kerning not applied)')
# Définissez le seuil de crénage afin que la taille de police actuelle du générateur soit au-dessus.
# Tout texte que nous ajoutons à partir de ce point aura le crénage appliqué. Les espaces entre les caractères
# seront ajustés, ce qui donne généralement une exécution de texte légèrement plus esthétique.
builder.font.kerning = 12
builder.writeln('TALLY. (Kerning applied)')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Kerning.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

