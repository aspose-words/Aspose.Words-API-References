---
title: PageSetup.endnote_options property
linktitle: endnote_options property
articleTitle: endnote_options property
second_title: Aspose.Words for Python
description: "PageSetup.endnote_options property. Provides options that control numbering and positioning of endnotes in this section."
type: docs
weight: 120
url: /fr/python-net/aspose.words/pagesetup/endnote_options/
---

## PageSetup.endnote_options property

Provides options that control numbering and positioning of endnotes in this section.


```python
@property
def endnote_options(self) -> aspose.words.notes.EndnoteOptions:
    ...

```

### Examples

Shows how to configure options affecting footnotes/endnotes in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote reference text.')
# Configurez toutes les notes de bas de page de la première section pour recommencer la numérotation à partir de 1
# à chaque nouvelle page et les afficher directement sous le texte sur chaque page.
footnote_options = doc.sections[0].page_setup.footnote_options
footnote_options.position = aw.notes.FootnotePosition.BENEATH_TEXT
footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
footnote_options.start_number = 1
builder.write(' Hello again.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Endnote reference text.')
# Configurez toutes les notes de fin de la première section pour maintenir un décompte continu tout au long de la section,
# en commençant à partir de 1. De plus, configurez-les toutes pour qu'elles apparaissent regroupées à la fin du document.
endnote_options = doc.sections[0].page_setup.endnote_options
endnote_options.position = aw.notes.EndnotePosition.END_OF_DOCUMENT
endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.CONTINUOUS
endnote_options.start_number = 1
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.FootnoteOptions.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

