---
title: FootnoteSeparatorType enumeration
linktitle: FootnoteSeparatorType enumeration
articleTitle: FootnoteSeparatorType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteSeparatorType enumeration. Specifies the type of the footnote/endnote separator."
type: docs
weight: 90
url: /python-net/aspose.words.notes/footnoteseparatortype/
---

## FootnoteSeparatorType enumeration

Specifies the type of the footnote/endnote separator.


### Members

| Name | Description |
| --- | --- |
| FOOTNOTE_SEPARATOR | Separator between main text and footnote text. |
| FOOTNOTE_CONTINUATION_SEPARATOR | Printed above footnote text on a page when the text must be continued from a previous page. |
| FOOTNOTE_CONTINUATION_NOTICE | Printed below footnote text on a page when footnote text must be continued on a succeeding page. |
| ENDNOTE_SEPARATOR | Separator between main text and endnote text. |
| ENDNOTE_CONTINUATION_SEPARATOR | Printed above endnote text on a page when the text must be continued from a previous page. |
| ENDNOTE_CONTINUATION_NOTICE | Printed below endnote text on a page when endnote text must be continued on a succeeding page. |

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

* module [aspose.words.notes](../)

