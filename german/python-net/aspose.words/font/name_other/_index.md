---
title: Font.name_other property
linktitle: name_other property
articleTitle: name_other property
second_title: Aspose.Words for Python
description: "Font.name_other property. Returns or sets the font used for characters with character codes from 128 through 255."
type: docs
weight: 270
url: /de/python-net/aspose.words/font/name_other/
---

## Font.name_other property

Returns or sets the font used for characters with character codes from 128 through 255.


```python
@property
def name_other(self) -> str:
    ...

@name_other.setter
def name_other(self, value: str):
    ...

```

### Examples

Shows how Microsoft Word can combine two different fonts in one run.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Angenommen, ein Run, den wir mit dem Builder einfügen, während wir diese Schriftkonfiguration verwenden
# enthält Zeichen innerhalb des ASCII‑Zeichenbereichs. In diesem Fall,
# Es wird diese Zeichen mit dieser Schriftart anzeigen.
builder.font.name_ascii = 'Calibri'
# Wenn keine andere Schriftart angegeben ist, wendet der Builder diese Schriftart ebenfalls auf alle Zeichen an, die er einfügt.
self.assertEqual('Calibri', builder.font.name)
# Geben Sie eine Schriftart an, die für alle Zeichen außerhalb des ASCII‑Bereichs verwendet wird.
# Idealerweise sollte diese Schriftart für jeden erforderlichen Nicht‑ASCII‑Zeichencode ein Glyph besitzen.
builder.font.name_other = 'Courier New'
# Fügen Sie einen Lauf ein, der ein Wort aus ASCII‑Zeichen enthält, und ein Wort mit allen Zeichen außerhalb dieses Bereichs.
# Jedes Zeichen wird je nach Schriftart angezeigt, abhängig davon.
builder.writeln('Hello, Привет')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NameAscii.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

