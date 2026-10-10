---
title: Font.italic_bi property
linktitle: italic_bi property
articleTitle: italic_bi property
second_title: Aspose.Words for Python
description: "Font.italic_bi property. True if the right-to-left text is formatted as italic."
type: docs
weight: 170
url: /it/python-net/aspose.words/font/italic_bi/
---

## Font.italic_bi property

True if the right-to-left text is formatted as italic.


```python
@property
def italic_bi(self) -> bool:
    ...

@italic_bi.setter
def italic_bi(self, value: bool):
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

