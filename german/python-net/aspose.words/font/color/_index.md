---
title: Font.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "Font.color property. Gets or sets the color of the font."
type: docs
weight: 70
url: /de/python-net/aspose.words/font/color/
---

## Font.color property

Gets or sets the color of the font.


```python
@property
def color(self) -> aspose.pydrawing.Color:
    ...

@color.setter
def color(self, value: aspose.pydrawing.Color):
    ...

```

### Examples

Shows how to insert formatted text using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Geben Sie die Schriftformatierung an und fügen Sie dann Text hinzu.
font = builder.font
font.size = 16
font.bold = True
font.color = aspose.pydrawing.Color.blue
font.name = 'Courier New'
font.underline = aw.Underline.DASH
builder.write('Hello world!')
```

Shows how to insert a hyperlink field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('For more information, please visit the ')
# Fügen Sie einen Hyperlink ein und heben Sie ihn mit benutzerdefinierter Formatierung hervor.
# Der Hyperlink ist ein anklickbarer Text, der uns zu dem in der URL angegebenen Ort führt.
builder.font.color = aspose.pydrawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink('Google website', 'https://www.google.com', False)
builder.font.clear_formatting()
builder.writeln('.')
# Strg + Linksklick auf den Link im Text in Microsoft Word öffnet die URL in einem neuen Browser‑Fenster.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertHyperlink.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

