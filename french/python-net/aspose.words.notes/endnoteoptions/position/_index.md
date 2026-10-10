---
title: EndnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "EndnoteOptions.position property. Specifies the endnotes position."
type: docs
weight: 20
url: /fr/python-net/aspose.words.notes/endnoteoptions/position/
---

## EndnoteOptions.position property

Specifies the endnotes position.


```python
@property
def position(self) -> aspose.words.notes.EndnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.EndnotePosition):
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Une note de fin est un moyen d'attacher une référence ou un commentaire marginal au texte
# qui n'interfère pas avec le flux du texte principal.
# L'insertion d'une note de fin ajoute un petit symbole de référence en exposant
# dans le texte principal à l'endroit où nous insérons la note de fin.
# Chaque note de fin crée également une entrée à la fin du document, composée d'un symbole
# qui correspond au symbole de référence dans le texte principal.
# Le texte de référence que nous transmettons à la méthode "InsertEndnote" du constructeur de document.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# Nous pouvons utiliser la propriété "Position" pour déterminer où le document placera toutes ses notes de fin.
# Si nous définissons la valeur de la propriété "Position" sur "EndnotePosition.EndOfDocument",
# toutes les notes de bas de page apparaîtront dans une collection à la fin du document. C'est la valeur par défaut.
# Si nous définissons la valeur de la propriété "Position" sur "EndnotePosition.EndOfSection",
# Chaque note de bas de page apparaîtra dans une collection à la fin de la section dont le texte contient le repère de référence de la note de fin.
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

