---
title: MarkdownLoadOptions constructor
linktitle: MarkdownLoadOptions constructor
articleTitle: MarkdownLoadOptions constructor
second_title: Aspose.Words for Python
description: "MarkdownLoadOptions constructor. Initializes a new instance of [MarkdownLoadOptions](../) class."
type: docs
weight: 10
url: /python-net/aspose.words.loading/markdownloadoptions/__init__/
---

## MarkdownLoadOptions() {#default}

Initializes a new instance of [MarkdownLoadOptions](../) class.



```python
def __init__(self):
    ...
```

### Remarks

Automatically sets [LoadFormat](../../../aspose.words/loadformat/) to [LoadFormat.MARKDOWN](../../../aspose.words/loadformat/#MARKDOWN).



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

