---
title: Font.scaling property
linktitle: scaling property
articleTitle: scaling property
second_title: Aspose.Words for Python
description: "Font.scaling property. Gets or sets character width scaling in percent."
type: docs
weight: 320
url: /de/python-net/aspose.words/font/scaling/
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
# Fügen Sie einen Text‑Run hinzu und erhöhen Sie die Zeichenbreite auf 150 %.
builder.font.scaling = 150
builder.writeln('Wide characters')
# Fügen Sie einen Text‑Run hinzu und fügen Sie zwischen jedem Zeichen 1 pt zusätzlichen horizontalen Abstand ein.
builder.font.spacing = 1
builder.writeln('Expanded by 1pt')
# Fügen Sie einen Text‑Run hinzu und bringen Sie die Zeichen um 1 pt näher zusammen.
builder.font.spacing = -1
builder.writeln('Condensed by 1pt')
doc.save(file_name=ARTIFACTS_DIR + 'Font.ScalingSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

