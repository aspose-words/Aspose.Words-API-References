---
title: FootnoteNumberingRule enumeration
linktitle: FootnoteNumberingRule enumeration
articleTitle: FootnoteNumberingRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteNumberingRule enumeration. Determines when automatic footnote or endnote numbering restarts."
type: docs
weight: 40
url: /fr/python-net/aspose.words.notes/footnotenumberingrule/
---

## FootnoteNumberingRule enumeration

Determines when automatic footnote or endnote numbering restarts.


### Members

| Name | Description |
| --- | --- |
| CONTINUOUS | Numbering continuous throughout the document. |
| RESTART_SECTION | Numbering restarts at each section. |
| RESTART_PAGE | Numbering restarts at each page. Valid for footnotes only. |
| DEFAULT | Equals [FootnoteNumberingRule.CONTINUOUS](./#CONTINUOUS). |

### Examples

Shows how to restart footnote/endnote numbering at certain places in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Les notes de bas de page et les notes de fin sont un moyen d’attacher une référence ou un commentaire secondaire au texte.
# qui n'interfère pas avec le flux du texte principal.
# Insérer une note de bas de page/une note de fin ajoute un petit symbole de référence en exposant.
# dans le texte principal où nous insérons la note de bas de page/la note de fin.
# Chaque note de bas de page/note de fin crée également une entrée, qui consiste en un symbole correspondant à la référence
# symbole dans le texte principal. Le texte de référence que nous transmettons à la méthode "InsertEndnote" du constructeur de document.
# Les entrées de notes de bas de page, par défaut, apparaissent en bas de chaque page qui contient
# leurs symboles de référence, et les notes de fin apparaissent à la fin du document.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 4.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 4.')
# Par défaut, le symbole de référence pour chaque note de bas de page et chaque note de fin est son indice
# parmi toutes les notes de bas de page/notes de fin du document. Chaque document maintient des comptes séparés
# pour les notes de bas de page et les notes de fin et ne redémarre jamais ces comptes.
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)
# Nous pouvons utiliser la propriété "RestartRule" pour faire redémarrer le document
# le comptage des notes de bas de page/notes de fin se fait sur une nouvelle page ou section.
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.NumberingRule.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)

