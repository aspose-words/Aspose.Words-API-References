---
title: Font.name_bi property
linktitle: name_bi property
articleTitle: name_bi property
second_title: Aspose.Words for Python
description: "Font.name_bi property. Returns or sets the name of the font in a right-to-left language document."
type: docs
weight: 250
url: /it/python-net/aspose.words/font/name_bi/
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
# Definisci un insieme di impostazioni di carattere per testo da sinistra a destra.
builder.font.name = 'Courier New'
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033  # en-US
# Definisci un altro insieme di impostazioni di carattere per testo da destra a sinistra.
builder.font.name_bi = 'Andalus'
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096  # ar-AR
# Possiamo usare la flag "bidi" per indicare se il testo che stiamo per aggiungere
# con il document builder è da destra a sinistra. Quando aggiungiamo testo con questa flag impostata su True,
# verrà formattato usando l'insieme di impostazioni di carattere da destra a sinistra.
builder.font.bidi = True
builder.write('مرحبًا')
# Imposta il flag su "False", e poi aggiungi testo da sinistra a destra.
# Il costruttore di documenti formatterà questi usando il set di impostazioni di carattere da sinistra a destra.
builder.font.bidi = False
builder.write(' Hello world!')
doc.save(ARTIFACTS_DIR + 'Font.bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

