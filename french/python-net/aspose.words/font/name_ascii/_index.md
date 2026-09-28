---
title: Font.name_ascii property
linktitle: name_ascii property
articleTitle: name_ascii property
second_title: Aspose.Words for Python
description: "Font.name_ascii property. Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127)."
type: docs
weight: 240
url: /fr/python-net/aspose.words/font/name_ascii/
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
# Supposons une exécution que nous utilisons le générateur pour insérer en utilisant cette configuration de police
# contient des caractères dans la plage des caractères ASCII. Dans ce cas,
# il affichera ces caractères en utilisant cette police.
builder.font.name_ascii = 'Calibri'
# Sans autre police spécifiée, le constructeur appliquera également cette police à tous les caractères qu'il insère.
self.assertEqual('Calibri', builder.font.name)
# Spécifiez une police à utiliser pour tous les caractères hors de la plage ASCII.
# Idéalement, cette police devrait contenir un glyphe pour chaque code de caractère non-ASCII requis.
builder.font.name_other = 'Courier New'
# Insérez un run avec un mot composé de caractères ASCII, et un mot avec tous les caractères hors de cette plage.
# Chaque caractère sera affiché en utilisant l'une ou l'autre des polices, selon.
builder.writeln('Hello, Привет')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NameAscii.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

