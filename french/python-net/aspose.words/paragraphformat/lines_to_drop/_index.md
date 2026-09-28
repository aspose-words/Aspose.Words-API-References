---
title: ParagraphFormat.lines_to_drop property
linktitle: lines_to_drop property
articleTitle: lines_to_drop property
second_title: Aspose.Words for Python
description: "ParagraphFormat.lines_to_drop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /fr/python-net/aspose.words/paragraphformat/lines_to_drop/
---

## ParagraphFormat.lines_to_drop property

Gets or sets the number of lines of the paragraph text used to calculate the drop cap height.


```python
@property
def lines_to_drop(self) -> int:
    ...

@lines_to_drop.setter
def lines_to_drop(self, value: int):
    ...

```

### Examples

Shows how to set the size of a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Modifiez la propriété "LinesToDrop" pour désigner un paragraphe comme lettrine,
# qui le transformera en une grande majuscule qui décorera le paragraphe suivant.
# Attribuez à cette propriété la valeur 4 pour donner à la lettrine une hauteur de quatre lignes de texte.
builder.paragraph_format.lines_to_drop = 4
builder.writeln('H')
# Réinitialisez la propriété "LinesToDrop" à 0 pour transformer le paragraphe suivant en un paragraphe ordinaire.
# Le texte de ce paragraphe s’enroulera autour de la lettrine.
builder.paragraph_format.lines_to_drop = 0
builder.writeln('ello world!')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LinesToDrop.odt')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

