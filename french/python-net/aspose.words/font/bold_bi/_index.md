---
title: Font.bold_bi property
linktitle: bold_bi property
articleTitle: bold_bi property
second_title: Aspose.Words for Python
description: "Font.bold_bi property. True if the right-to-left text is formatted as bold."
type: docs
weight: 50
url: /fr/python-net/aspose.words/font/bold_bi/
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
# Définissez un ensemble de paramètres de police pour le texte de gauche à droite.
builder.font.name = 'Courier New'
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033  # en-US
# Définissez un autre ensemble de paramètres de police pour le texte de droite à gauche.
builder.font.name_bi = 'Andalus'
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096  # ar-AR
# Nous pouvons utiliser le drapeau "bidi" pour indiquer si le texte que nous allons ajouter
# avec le DocumentBuilder est de droite à gauche. Lorsque nous ajoutons du texte avec ce drapeau réglé sur True,
# il sera formaté en utilisant l'ensemble de paramètres de police de droite à gauche.
builder.font.bidi = True
builder.write('مرحبًا')
# Définissez le drapeau sur "False", puis ajoutez du texte de gauche à droite.
# Le générateur de documents formatra ceux-ci en utilisant le jeu de paramètres de police de gauche à droite.
builder.font.bidi = False
builder.write(' Hello world!')
doc.save(ARTIFACTS_DIR + 'Font.bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

