---
title: MarkdownLoadOptions.import_underline_formatting property
linktitle: import_underline_formatting property
articleTitle: import_underline_formatting property
second_title: Aspose.Words for Python
description: "MarkdownLoadOptions.import_underline_formatting property. Gets or sets a boolean value indicating either to recognize a sequence of two plus characters ++ as underline text formatting"
type: docs
weight: 20
url: /python-net/aspose.words.loading/markdownloadoptions/import_underline_formatting/
---

## MarkdownLoadOptions.import_underline_formatting property

Gets or sets a boolean value indicating either to recognize a sequence
of two plus characters "++" as underline text formatting.
The default value is ``False``.



```python
@property
def import_underline_formatting(self) -> bool:
    ...

@import_underline_formatting.setter
def import_underline_formatting(self, value: bool):
    ...

```

### Examples

Shows how to recognize plus characters "++" as underline text formatting.

```python
with io.BytesIO(system_helper.text.Encoding.get_bytes('++12 and B++', system_helper.text.Encoding.ascii())) as stream:
    load_options = aw.loading.MarkdownLoadOptions()
    load_options.import_underline_formatting = True
    doc = aw.Document(stream=stream, load_options=load_options)
    para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
    self.assertEqual(aw.Underline.SINGLE, para.runs[0].font.underline)
    load_options = aw.loading.MarkdownLoadOptions()
    load_options.import_underline_formatting = False
    doc = aw.Document(stream=stream, load_options=load_options)
    para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
    self.assertEqual(aw.Underline.NONE, para.runs[0].font.underline)
```

### See Also

* module [aspose.words.loading](../../)
* class [MarkdownLoadOptions](../)

