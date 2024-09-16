---
title: DocumentBase.footnote_separators property
linktitle: footnote_separators property
articleTitle: footnote_separators property
second_title: Aspose.Words for Python
description: "DocumentBase.footnote_separators property. Provides access to the footnote/endnote separators defined in the document."
type: docs
weight: 40
url: /python-net/aspose.words/documentbase/footnote_separators/
---

## DocumentBase.footnote_separators property

Provides access to the footnote/endnote separators defined in the document.


```python
@property
def footnote_separators(self) -> aspose.words.notes.FootnoteSeparatorCollection:
    ...

```

### Examples

Shows how to remove endnote separator.

```python
doc = aw.Document(file_name=MY_DIR + 'Footnotes and endnotes.docx')
endnote_separator = doc.footnote_separators.get_by_footnote_separator_type(aw.notes.FootnoteSeparatorType.ENDNOTE_SEPARATOR)
# Remove endnote separator.
endnote_separator.first_paragraph.first_child.remove()
```

Shows how to manage footnote separator format.

```python
doc = aw.Document(file_name=MY_DIR + 'Footnotes and endnotes.docx')
footnote_separator = doc.footnote_separators.get_by_footnote_separator_type(aw.notes.FootnoteSeparatorType.FOOTNOTE_SEPARATOR)
# Align footnote separator.
footnote_separator.first_paragraph.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)

