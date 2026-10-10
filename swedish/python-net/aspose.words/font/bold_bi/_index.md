---
title: Font.bold_bi property
linktitle: bold_bi property
articleTitle: bold_bi property
second_title: Aspose.Words for Python
description: "Font.bold_bi property. True if the right-to-left text is formatted as bold."
type: docs
weight: 50
url: /sv/python-net/aspose.words/font/bold_bi/
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
# Definiera en uppsättning teckensnittsinställningar för vänster-till-höger-text.
builder.font.name = 'Courier New'
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033  # en-US
# Definiera en annan uppsättning teckensnittsinställningar för höger-till-vänster-text.
builder.font.name_bi = 'Andalus'
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096  # ar-AR
# Vi kan använda flaggan "bidi" för att indikera om texten vi håller på att lägga till
# med dokumentbyggaren är höger-till-vänster. När vi lägger till text med denna flagga satt till True,
# kommer den att formateras med den höger-till-vänster-uppsättningen av teckensnittsinställningar.
builder.font.bidi = True
builder.write('مرحبًا')
# Ställ flaggan till "False", och lägg sedan till vänster-till-höger-text.
# Dokumentbyggaren kommer att formatera dessa med den vänster-till-höger uppsättningen av teckensnittsinställningar.
builder.font.bidi = False
builder.write(' Hello world!')
doc.save(ARTIFACTS_DIR + 'Font.bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

