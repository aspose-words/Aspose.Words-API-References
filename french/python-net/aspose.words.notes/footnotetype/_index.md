---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 100
url: /fr/python-net/aspose.words.notes/footnotetype/
---

## FootnoteType enumeration

Specifies whether this is a footnote or an endnote.

Both footnotes and endnotes are represented by objects by the [FootnoteType.FOOTNOTE](./#FOOTNOTE)
class. Use [Footnote.footnote_type](../footnote/footnote_type/) to distinguish between footnotes 
and endnotes.




### Members

| Name | Description |
| --- | --- |
| FOOTNOTE | The object is a footnote. |
| ENDNOTE | The object is an endnote. |

### Examples

Shows how to reference text with a footnote and an endnote.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérez du texte et marquez-le avec une note de bas de page dont la propriété IsAuto est définie sur "true" par défaut,
# ainsi le marqueur visible dans le texte principal sera automatiquement numéroté à "1",
# et la note de bas de page apparaîtra en bas de la page.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# Insérez plus de texte et marquez-le avec une note de fin avec une marque de référence personnalisée,
# qui sera utilisée à la place du numéro "2" et définira "IsAuto" sur false.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# Les notes de bas de page apparaissent toujours en bas du texte auquel elles se réfèrent,
# ainsi ce saut de page n'affectera pas la note de bas de page.
# En revanche, les notes de fin sont toujours à la fin du document
# de sorte que ce saut de page déplacera la note de fin à la page suivante.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

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

* module [aspose.words.notes](../)
* enum value [FootnoteType.FOOTNOTE](./#FOOTNOTE)

