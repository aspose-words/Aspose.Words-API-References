---
title: Document.footnote_options property
linktitle: footnote_options property
articleTitle: footnote_options property
second_title: Aspose.Words for Python
description: "Document.footnote_options property. Provides options that control numbering and positioning of footnotes in this document."
type: docs
weight: 160
url: /fr/python-net/aspose.words/document/footnote_options/
---

## Document.footnote_options property

Provides options that control numbering and positioning of footnotes in this document.


```python
@property
def footnote_options(self) -> aspose.words.notes.FootnoteOptions:
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

Shows how to change the number style of footnote/endnote reference marks.

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
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.', reference_mark='Custom footnote reference mark')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.', reference_mark='Custom endnote reference mark')
# Par défaut, le symbole de référence pour chaque note de bas de page et chaque note de fin est son indice
# parmi toutes les notes de bas de page/notes de fin du document. Chaque document maintient des comptes séparés
# pour les notes de bas de page et pour les notes de fin. Par défaut, les notes de bas de page affichent leurs numéros en chiffres arabes,
# et les notes de fin affichent leurs numéros en chiffres romains minuscules.
self.assertEqual(aw.NumberStyle.ARABIC, doc.footnote_options.number_style)
self.assertEqual(aw.NumberStyle.LOWERCASE_ROMAN, doc.endnote_options.number_style)
# Nous pouvons utiliser la propriété "NumberStyle" pour appliquer des styles de numérotation personnalisés aux notes de bas de page et aux notes de fin.
# Cela n’affectera pas les notes de bas de page/notes de fin avec des repères de référence personnalisés.
doc.footnote_options.number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc.endnote_options.number_style = aw.NumberStyle.UPPERCASE_LETTER
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.RefMarkNumberStyle.docx')
```

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

* module [aspose.words](../../)
* class [Document](../)

