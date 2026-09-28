---
title: PageSetup.endnote_options property
linktitle: endnote_options property
articleTitle: endnote_options property
second_title: Aspose.Words for Python
description: "PageSetup.endnote_options property. Provides options that control numbering and positioning of endnotes in this section."
type: docs
weight: 120
url: /ar/python-net/aspose.words/pagesetup/endnote_options/
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
# قم بتهيئة جميع الحواشي السفلية في القسم الأول لإعادة بدء الترقيم من 1
# في كل صفحة جديدة وعرضها مباشرةً تحت النص في كل صفحة.
footnote_options = doc.sections[0].page_setup.footnote_options
footnote_options.position = aw.notes.FootnotePosition.BENEATH_TEXT
footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
footnote_options.start_number = 1
builder.write(' Hello again.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Endnote reference text.')
# قم بتهيئة جميع الحواشي الختامية في القسم الأول للحفاظ على عدّ مستمر طوال القسم،
# بدءًا من 1. أيضًا، قم بتعيينها جميعًا لتظهر مجمّعة في نهاية المستند.
endnote_options = doc.sections[0].page_setup.endnote_options
endnote_options.position = aw.notes.EndnotePosition.END_OF_DOCUMENT
endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.CONTINUOUS
endnote_options.start_number = 1
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.FootnoteOptions.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

