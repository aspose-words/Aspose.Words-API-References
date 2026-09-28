---
title: Font.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for Python
description: "Font.kerning property. Gets or sets the font size at which kerning starts."
type: docs
weight: 180
url: /de/python-net/aspose.words/font/kerning/
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
# Legen Sie die Schriftgröße des Builders fest sowie die Mindestgröße, ab der Kerning wirksam wird.
# Die Schriftgröße fällt unter die Kerning‑Schwelle, sodass der nachfolgende Run kein Kerning hat.
builder.font.size = 18
builder.font.kerning = 24
builder.writeln('TALLY. (Kerning not applied)')
# Setzen Sie die Kerning‑Schwelle so, dass die aktuelle Schriftgröße des Builders darüber liegt.
# Jeder Text, den wir ab diesem Punkt hinzufügen, wird mit Kerning versehen. Die Abstände zwischen den Zeichen
# werden angepasst, was normalerweise zu einem leicht ästhetisch ansprechenderen Text‑Run führt.
builder.font.kerning = 12
builder.writeln('TALLY. (Kerning applied)')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Kerning.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

