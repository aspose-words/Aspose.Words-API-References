---
title: Font.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for Python
description: "Font.kerning property. Gets or sets the font size at which kerning starts."
type: docs
weight: 180
url: /it/python-net/aspose.words/font/kerning/
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
# Imposta la dimensione del carattere del costruttore e la dimensione minima a cui il kerning avrà effetto.
# La dimensione del carattere scende sotto la soglia di kerning, quindi il run sottostante non avrà kerning.
builder.font.size = 18
builder.font.kerning = 24
builder.writeln('TALLY. (Kerning not applied)')
# Imposta la soglia di kerning in modo che la dimensione attuale del carattere del costruttore sia sopra di essa.
# Qualsiasi testo aggiungiamo da questo punto avrà il kerning applicato. Gli spazi tra i caratteri
# saranno regolati, normalmente risultando in un run di testo leggermente più estetico.
builder.font.kerning = 12
builder.writeln('TALLY. (Kerning applied)')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Kerning.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

