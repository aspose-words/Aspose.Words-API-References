---
title: FootnoteOptions.start_number property
linktitle: start_number property
articleTitle: start_number property
second_title: Aspose.Words for Python
description: "FootnoteOptions.start_number property. Specifies the starting number or character for the first automatically numbered footnotes."
type: docs
weight: 50
url: /fr/python-net/aspose.words.notes/footnoteoptions/start_number/
---

## FootnoteOptions.start_number property

Specifies the starting number or character for the first automatically numbered footnotes.


```python
@property
def start_number(self) -> int:
    ...

@start_number.setter
def start_number(self, value: int):
    ...

```

### Remarks

This property has effect only when [FootnoteOptions.restart_rule](../restart_rule/) is set to
[FootnoteNumberingRule.CONTINUOUS](../../footnotenumberingrule/#CONTINUOUS).




### Examples

Shows how to set a number at which the document begins the footnote/endnote count.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Les notes de bas de page et les notes de fin sont un moyen d’attacher une référence ou un commentaire secondaire au texte.
# qui n'interfère pas avec le flux du texte principal.
# Insérer une note de bas de page/une note de fin ajoute un petit symbole de référence en exposant.
# dans le texte principal où nous insérons la note de bas de page/la note de fin.
# Chaque note de bas de page/note de fin crée également une entrée, qui consiste en un symbole
# qui correspond au symbole de référence dans le texte principal.
# Le texte de référence que nous transmettons à la méthode "InsertEndnote" du constructeur de document.
# Les entrées de notes de bas de page, par défaut, apparaissent en bas de chaque page qui contient
# leurs symboles de référence, et les notes de fin apparaissent à la fin du document.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
# Par défaut, le symbole de référence pour chaque note de bas de page et chaque note de fin est son indice
# parmi toutes les notes de bas de page/notes de fin du document. Chaque document maintient des comptes séparés
# pour les notes de bas de page et les notes de fin, qui commencent toutes deux à 1.
self.assertEqual(1, doc.footnote_options.start_number)
self.assertEqual(1, doc.endnote_options.start_number)
# Nous pouvons utiliser la propriété "StartNumber" pour faire que le document
# commence le comptage d'une note de bas de page ou d'une note de fin à un nombre différent.
doc.endnote_options.number_style = aw.NumberStyle.ARABIC
doc.endnote_options.start_number = 50
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.StartNumber.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

