---
title: EndnoteOptions.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "EndnoteOptions.number_style property. Specifies the number format for automatically numbered endnotes."
type: docs
weight: 10
url: /fr/python-net/aspose.words.notes/endnoteoptions/number_style/
---

## EndnoteOptions.number_style property

Specifies the number format for automatically numbered endnotes.


```python
@property
def number_style(self) -> aspose.words.NumberStyle:
    ...

@number_style.setter
def number_style(self, value: aspose.words.NumberStyle):
    ...

```

### Remarks

Not all number styles are applicable for this property. For the list of applicable
number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select
a number style that is not applicable, Microsoft Word will revert to a default value.




### Examples

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

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

