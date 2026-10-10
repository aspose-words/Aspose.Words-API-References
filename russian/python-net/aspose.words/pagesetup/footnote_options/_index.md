---
title: PageSetup.footnote_options property
linktitle: footnote_options property
articleTitle: footnote_options property
second_title: Aspose.Words for Python
description: "PageSetup.footnote_options property. Provides options that control numbering and positioning of footnotes in this section."
type: docs
weight: 150
url: /ru/python-net/aspose.words/pagesetup/footnote_options/
---

## PageSetup.footnote_options property

Provides options that control numbering and positioning of footnotes in this section.


```python
@property
def footnote_options(self) -> aspose.words.notes.FootnoteOptions:
    ...

```

### Examples

Shows how to configure options affecting footnotes/endnotes in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote reference text.')
# Настройте все сноски в первом разделе так, чтобы нумерация начиналась с 1
# на каждой новой странице и отображались непосредственно под текстом на каждой странице.
footnote_options = doc.sections[0].page_setup.footnote_options
footnote_options.position = aw.notes.FootnotePosition.BENEATH_TEXT
footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
footnote_options.start_number = 1
builder.write(' Hello again.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Endnote reference text.')
# Настройте все концевые сноски в первом разделе так, чтобы сохранялся непрерывный счет по всему разделу,
# начиная с 1. Также настройте их так, чтобы они собирались в конце документа.
endnote_options = doc.sections[0].page_setup.endnote_options
endnote_options.position = aw.notes.EndnotePosition.END_OF_DOCUMENT
endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.CONTINUOUS
endnote_options.start_number = 1
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.FootnoteOptions.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

