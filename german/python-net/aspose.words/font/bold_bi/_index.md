---
title: Font.bold_bi property
linktitle: bold_bi property
articleTitle: bold_bi property
second_title: Aspose.Words for Python
description: "Font.bold_bi property. True if the right-to-left text is formatted as bold."
type: docs
weight: 50
url: /de/python-net/aspose.words/font/bold_bi/
---

## Font.bold_bi property

True if the right-to-left text is formatted as bold.


```python
@property
def bold_bi(self) -> bool:
    ...

@bold_bi.setter
def bold_bi(self, value: bool):
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

