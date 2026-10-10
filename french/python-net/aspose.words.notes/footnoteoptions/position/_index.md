---
title: FootnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "FootnoteOptions.position property. Specifies the footnotes position."
type: docs
weight: 30
url: /fr/python-net/aspose.words.notes/footnoteoptions/position/
---

## FootnoteOptions.position property

Specifies the footnotes position.


```python
@property
def position(self) -> aspose.words.notes.FootnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.FootnotePosition):
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Une note de bas de page est un moyen d’attacher une référence ou un commentaire secondaire au texte.
# qui n'interfère pas avec le flux du texte principal.
# Insérer une note de bas de page ajoute un petit symbole de référence en exposant.
# dans le texte principal où nous insérons la note de bas de page.
# Chaque note de bas de page crée également une entrée en bas de la page, composée d’un symbole
# qui correspond au symbole de référence dans le texte principal.
# Le texte de référence que nous transmettons à la méthode "InsertFootnote" du constructeur de document.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote contents.')
# Nous pouvons utiliser la propriété "Position" pour déterminer où le document placera toutes ses notes de bas de page.
# Si nous définissons la valeur de la propriété "Position" sur "FootnotePosition.BottomOfPage",
# Chaque note de bas de page apparaîtra en bas de la page qui contient son repère de référence. C’est la valeur par défaut.
# Si nous définissons la valeur de la propriété "Position" sur "FootnotePosition.BeneathText",
# Chaque note de bas de page apparaîtra à la fin du texte de la page qui contient son repère de référence.
doc.footnote_options.position = footnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionFootnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

