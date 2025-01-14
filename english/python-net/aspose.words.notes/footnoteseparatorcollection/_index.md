---
title: FootnoteSeparatorCollection class
linktitle: FootnoteSeparatorCollection class
articleTitle: FootnoteSeparatorCollection class
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteSeparatorCollection class. Provides typed access to [FootnoteSeparator](../footnoteseparator/) nodes of a document."
type: docs
weight: 80
url: /python-net/aspose.words.notes/footnoteseparatorcollection/
---

## FootnoteSeparatorCollection class

Provides typed access to [FootnoteSeparator](../footnoteseparator/) nodes of a document.



### Constructors
| Name | Description |
| --- | --- |
| [FootnoteSeparatorCollection()](./__init__/#default) | The default constructor. |

### Methods

| Name | Description |
| --- | --- |
|[ get_by_footnote_separator_type(separator_type)](./get_by_footnote_separator_type/#footnoteseparatortype) | Retrieves a [FootnoteSeparator](../footnoteseparator/) of the specified type. |

### Examples

Shows how to manage footnote separator format.

```python
doc = aw.Document(file_name=MY_DIR + 'Footnotes and endnotes.docx')
footnote_separator = doc.footnote_separators.get_by_footnote_separator_type(aw.notes.FootnoteSeparatorType.FOOTNOTE_SEPARATOR)
# Align footnote separator.
footnote_separator.first_paragraph.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
```

### See Also

* module [aspose.words.notes](../)

