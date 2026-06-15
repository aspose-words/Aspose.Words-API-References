---
title: FindReplaceOptions.ignore_footnotes property
linktitle: ignore_footnotes property
articleTitle: ignore_footnotes property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_footnotes property. Gets or sets a boolean value indicating either to ignore footnotes"
type: docs
weight: 90
url: /python-net/aspose.words.replacing/findreplaceoptions/ignore_footnotes/
---

## FindReplaceOptions.ignore_footnotes property

Gets or sets a boolean value indicating either to ignore footnotes.
The default value is ``False``.



```python
@property
def ignore_footnotes(self) -> bool:
    ...

@ignore_footnotes.setter
def ignore_footnotes(self, value: bool):
    ...

```

### Examples

Shows how to ignore footnotes during a find-and-replace operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Lorem ipsum dolor sit amet, consectetur adipiscing elit.')
builder.insert_paragraph()
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Lorem ipsum dolor sit amet, consectetur adipiscing elit.')
# Set the "IgnoreFootnotes" flag to "true" to get the find-and-replace
# operation to ignore text inside footnotes.
# Set the "IgnoreFootnotes" flag to "false" to get the find-and-replace
# operation to also search for text inside footnotes.
options = aw.replacing.FindReplaceOptions()
options.ignore_footnotes = is_ignore_footnotes
doc.range.replace(pattern='Lorem ipsum', replacement='Replaced Lorem ipsum', options=options)
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

