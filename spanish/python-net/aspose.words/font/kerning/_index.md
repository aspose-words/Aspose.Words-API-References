---
title: Font.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for Python
description: "Font.kerning property. Gets or sets the font size at which kerning starts."
type: docs
weight: 180
url: /es/python-net/aspose.words/font/kerning/
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
# Establezca el tamaño de fuente del generador y el tamaño mínimo en el que el kerning tendrá efecto.
# El tamaño de fuente cae por debajo del umbral de kerning, por lo que el run siguiente no tendrá kerning.
builder.font.size = 18
builder.font.kerning = 24
builder.writeln('TALLY. (Kerning not applied)')
# Establezca el umbral de kerning para que el tamaño de fuente actual del generador esté por encima de él.
# Cualquier texto que añadamos a partir de este punto tendrá kerning aplicado. Los espacios entre caracteres
# serán ajustados, normalmente resultando en un run de texto ligeramente más estéticamente agradable.
builder.font.kerning = 12
builder.writeln('TALLY. (Kerning applied)')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Kerning.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

