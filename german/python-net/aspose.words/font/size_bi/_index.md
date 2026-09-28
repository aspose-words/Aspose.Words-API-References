---
title: Font.size_bi property
linktitle: size_bi property
articleTitle: size_bi property
second_title: Aspose.Words for Python
description: "Font.size_bi property. Gets or sets the font size in points used in a right-to-left document."
type: docs
weight: 360
url: /de/python-net/aspose.words/font/size_bi/
---

## Font.size_bi property

Gets or sets the font size in points used in a right-to-left document.


```python
@property
def size_bi(self) -> float:
    ...

@size_bi.setter
def size_bi(self, value: float):
    ...

```

### Examples

Shows how to define separate sets of font settings for right-to-left, and right-to-left text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Definieren Sie ein Satz von Schriftarteinstellungen für Links-nach-Rechts-Text.
builder.font.name = 'Courier New'
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033  # en-US
# Definieren Sie einen weiteren Satz von Schriftarteinstellungen für Rechts-nach-Links-Text.
builder.font.name_bi = 'Andalus'
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096  # ar-AR
# Wir können das "bidi"-Flag verwenden, um anzugeben, ob der Text, den wir hinzufügen wollen
# mit dem DocumentBuilder, von rechts nach links verläuft. Wenn wir Text mit diesem Flag auf True setzen,
# wird er mit dem Rechts-nach-Links-Satz von Schriftarteinstellungen formatiert.
builder.font.bidi = True
builder.write('مرحبًا')
# Setzen Sie das Flag auf "False" und fügen Sie dann links-nach-rechts-Text hinzu.
# Der Dokument-Builder formatiert diese mithilfe des links-nach-rechts-Font‑Einstellungssets.
builder.font.bidi = False
builder.write(' Hello world!')
doc.save(ARTIFACTS_DIR + 'Font.bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

