---
title: Footnote.is_auto property
linktitle: is_auto property
articleTitle: is_auto property
second_title: Aspose.Words for Python
description: "Footnote.is_auto property. Holds a value that specifies whether this is a auto-numbered footnote or  footnote with user defined custom reference mark."
type: docs
weight: 40
url: /fr/python-net/aspose.words.notes/footnote/is_auto/
---

## Footnote.is_auto property

Holds a value that specifies whether this is a auto-numbered footnote or 
footnote with user defined custom reference mark.


```python
@property
def is_auto(self) -> bool:
    ...

@is_auto.setter
def is_auto(self, value: bool):
    ...

```

### Remarks

[Footnote.reference_mark](../reference_mark/) initialized with empty string if [Footnote.is_auto](./) set to ``False``.



### Examples

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ajoutez du texte et référencez-le avec une note de bas de page. Cette note de bas de page placera une petite référence en exposant
# après le texte qu'elle référence et créera une entrée sous le texte principal en bas de la page.
# Cette entrée contiendra la marque de référence de la note de bas de page et le texte de référence,
# que nous transmettrons à la méthode "InsertFootnote" du générateur de documents.
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Si cette propriété est définie sur "true", alors la marque de référence de notre note de bas de page
# sera son indice parmi toutes les notes de bas de page de la section.
# Ceci est la première note de bas de page, donc la marque de référence sera "1".
self.assertTrue(footnote.is_auto)
# Nous pouvons déplacer le générateur de documents à l'intérieur de la note de bas de page pour modifier son texte de référence.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Nous pouvons définir une marque de référence personnalisée que la note de bas de page utilisera à la place de son numéro d'indice.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# Un signet avec le drapeau "IsAuto" défini sur true affichera toujours son index réel
# même si les signets précédents affichent des marques de référence personnalisées, la marque de référence de ce signet sera un "3".
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.AddFootnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

