---
title: Font.locale_id_bi property
linktitle: locale_id_bi property
articleTitle: locale_id_bi property
second_title: Aspose.Words for Python
description: "Font.locale_id_bi property. Gets or sets the locale identifier (language) of the formatted right-to-left characters."
type: docs
weight: 210
url: /it/python-net/aspose.words/font/locale_id_bi/
---

## Font.locale_id_bi property

Gets or sets the locale identifier (language) of the formatted right-to-left characters.


```python
@property
def locale_id_bi(self) -> int:
    ...

@locale_id_bi.setter
def locale_id_bi(self, value: int):
    ...

```

### Remarks

For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx


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

