---
title: MarkdownLoadOptions.soft_line_break_character property
linktitle: soft_line_break_character property
articleTitle: soft_line_break_character property
second_title: Aspose.Words for Python
description: "MarkdownLoadOptions.soft_line_break_character property. Gets or sets a character value representing `soft line break`"
type: docs
weight: 40
url: /python-net/aspose.words.loading/markdownloadoptions/soft_line_break_character/
---

## MarkdownLoadOptions.soft_line_break_character property

Gets or sets a character value representing `soft line break`.
The default value is ``SPACE (U+0020)``.



```python
@property
def soft_line_break_character(self) -> str:
    ...

@soft_line_break_character.setter
def soft_line_break_character(self, value: str):
    ...

```

### Remarks

Note, setting this option to [ControlChar.LINE_BREAK_CHAR](../../../aspose.words/controlchar/LINE_BREAK_CHAR/) allows you
to load soft line breaks as hard line breaks.



### Examples

Shows how to set soft line break character.

```python
with io.BytesIO(system_helper.text.Encoding.get_bytes('line1\nline2', system_helper.text.Encoding.utf_8())) as stream:
    load_options = aw.loading.MarkdownLoadOptions()
    load_options.soft_line_break_character = aw.ControlChar.LINE_BREAK_CHAR
    doc = aw.Document(stream=stream, load_options=load_options)
    self.assertEqual('line1\x0bline2', doc.get_text().strip())
```

### See Also

* module [aspose.words.loading](../../)
* class [MarkdownLoadOptions](../)

