---
title: Font.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "Font.hidden property. True if the font is formatted as hidden text."
type: docs
weight: 140
url: /zh/python-net/aspose.words/font/hidden/
---

## Font.hidden property

True if the font is formatted as hidden text.


```python
@property
def hidden(self) -> bool:
    ...

@hidden.setter
def hidden(self, value: bool):
    ...

```

### Examples

Shows how to create a run of hidden text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 将 Hidden 标志设置为 true 时，使用此 Font 对象创建的任何文本将在文档中不可见。
# 除非我们启用“Hidden text”选项，否则我们将看不到或突出显示隐藏文本
# 该选项位于 Microsoft Word 的 “File” -> “Options” -> “Display”。文本仍然存在，
# 并且我们可以通过编程方式访问此文本。
# 不建议使用此方法隐藏敏感信息。
builder.font.hidden = True
builder.font.size = 36
builder.writeln('This text will not be visible in the document.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Hidden.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

