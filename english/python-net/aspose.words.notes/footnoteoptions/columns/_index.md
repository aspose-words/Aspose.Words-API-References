---
title: FootnoteOptions.columns property
linktitle: columns property
articleTitle: columns property
second_title: Aspose.Words for Python
description: "FootnoteOptions.columns property. Specifies the number of columns with which the footnotes area is formatted."
type: docs
weight: 10
url: /python-net/aspose.words.notes/footnoteoptions/columns/
---

## FootnoteOptions.columns property

Specifies the number of columns with which the footnotes area is formatted.


```python
@property
def columns(self) -> int:
    ...

@columns.setter
def columns(self, value: int):
    ...

```

### Remarks

If this property has the value of 0, the footnotes area is formatted with a number of columns based on
the number of columns on the displayed page. The default value is 0.


### Examples

Shows how to split the footnote section into a given number of columns.

```python
doc = aw.Document(MY_DIR + "Footnotes and endnotes.docx")

doc.footnote_options.columns = 2
doc.save(ARTIFACTS_DIR + "Document.footnote_columns.docx")
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

