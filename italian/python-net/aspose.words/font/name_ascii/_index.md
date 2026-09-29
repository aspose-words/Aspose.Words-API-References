---
title: Font.name_ascii property
linktitle: name_ascii property
articleTitle: name_ascii property
second_title: Aspose.Words for Python
description: "Font.name_ascii property. Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127)."
type: docs
weight: 240
url: /it/python-net/aspose.words/font/name_ascii/
---

## Font.name_ascii property

Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127).


```python
@property
def name_ascii(self) -> str:
    ...

@name_ascii.setter
def name_ascii(self, value: str):
    ...

```

### Examples

Shows how Microsoft Word can combine two different fonts in one run.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Supponiamo un run che usiamo il costruttore per inserire usando questa configurazione di carattere
# contiene caratteri all'interno dell'intervallo dei caratteri ASCII. In tal caso,
# visualizzerà quei caratteri usando questo font.
builder.font.name_ascii = 'Calibri'
# Se non viene specificato alcun altro font, il builder applicherà anche questo font a tutti i caratteri che inserisce.
self.assertEqual('Calibri', builder.font.name)
# Specifica un font da utilizzare per tutti i caratteri al di fuori dell'intervallo ASCII.
# Idealmente, questo font dovrebbe avere un glifo per ogni codice di carattere non ASCII richiesto.
builder.font.name_other = 'Courier New'
# Inserisci un run con una parola composta da caratteri ASCII e una parola con tutti i caratteri al di fuori di quell'intervallo.
# Ogni carattere verrà visualizzato usando uno dei due font, a seconda di.
builder.writeln('Hello, Привет')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NameAscii.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

