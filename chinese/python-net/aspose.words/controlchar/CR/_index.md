---
title: ControlChar.CR property
linktitle: CR property
articleTitle: CR property
second_title: Aspose.Words for Python
description: "ControlChar.CR property. Carriage return character: \\x000d or \\r"
type: docs
weight: 50
url: /zh/python-net/aspose.words/controlchar/CR/
---

## ControlChar.CR property

Carriage return character: "\\x000d" or "\\r". Same as [ControlChar.PARAGRAPH_BREAK](../PARAGRAPH_BREAK/).



```python
@property
def CR(self) -> str:
    ...

```

### Examples

Shows how to use control characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 使用 DocumentBuilder 插入带文本的段落。
builder.writeln('Hello world!')
builder.writeln('Hello again!')
# 将文档转换为文本形式会显示控制字符
# 表示文档的一些结构元素，例如分页符。
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + f'Hello again!{aw.ControlChar.CR}' + aw.ControlChar.PAGE_BREAK, doc.get_text())
# 将文档转换为字符串形式时，
# 我们可以使用 Trim 方法省略部分控制字符。
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + 'Hello again!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [ControlChar](../)

