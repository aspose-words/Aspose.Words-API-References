---
title: MarkdownLoadOptions.preserve_empty_lines property
linktitle: preserve_empty_lines property
articleTitle: preserve_empty_lines property
second_title: Aspose.Words for Python
description: "MarkdownLoadOptions.preserve_empty_lines property. Gets or sets a boolean value indicating whether to preserve empty lines while load a [LoadFormat.MARKDOWN](../../../aspose.words/loadformat/#MARKDOWN) document"
type: docs
weight: 30
url: /python-net/aspose.words.loading/markdownloadoptions/preserve_empty_lines/
---

## MarkdownLoadOptions.preserve_empty_lines property

Gets or sets a boolean value indicating whether to preserve empty lines while load a [LoadFormat.MARKDOWN](../../../aspose.words/loadformat/#MARKDOWN) document.
The default value is ``False``.
Normally, empty lines between block-level elements in Markdown are ignored. Empty lines at the beginning and
end of the document are also ignored. This option allows to import such empty lines.




```python
@property
def preserve_empty_lines(self) -> bool:
    ...

@preserve_empty_lines.setter
def preserve_empty_lines(self, value: bool):
    ...

```

### Examples

Shows how to preserve empty line while load a document.

```python
md_text = f'{system_helper.environment.Environment.new_line()}Line1{system_helper.environment.Environment.new_line()}{system_helper.environment.Environment.new_line()}Line2{system_helper.environment.Environment.new_line()}{system_helper.environment.Environment.new_line()}'
with io.BytesIO(system_helper.text.Encoding.get_bytes(md_text, system_helper.text.Encoding.utf_8())) as stream:
    load_options = aw.loading.MarkdownLoadOptions()
    load_options.preserve_empty_lines = True
    doc = aw.Document(stream=stream, load_options=load_options)
    self.assertEqual('\rLine1\r\rLine2\r\x0c', doc.get_text())
```

### See Also

* module [aspose.words.loading](../../)
* class [MarkdownLoadOptions](../)

