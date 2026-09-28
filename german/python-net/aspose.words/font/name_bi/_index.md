---
title: Font.name_bi property
linktitle: name_bi property
articleTitle: name_bi property
second_title: Aspose.Words for Python
description: "Font.name_bi property. Returns or sets the name of the font in a right-to-left language document."
type: docs
weight: 250
url: /de/python-net/aspose.words/font/name_bi/
---

## Font.name_bi property

Returns or sets the name of the font in a right-to-left language document.


```python
@property
def name_bi(self) -> str:
    ...

@name_bi.setter
def name_bi(self, value: str):
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
* property [Font.name](../name/)

