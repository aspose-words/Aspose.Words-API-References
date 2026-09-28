---
title: StyleCollection indexer
linktitle: StyleCollection indexer
articleTitle: StyleCollection indexer
second_title: Aspose.Words for Python
description: "StyleCollection indexer. Gets a style by index."
type: docs
weight: 10
url: /zh/python-net/aspose.words/stylecollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets a style by index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to add a Style to a document's styles collection.

```python
doc = aw.Document()
styles = doc.styles
# 为我们以后可能添加到此集合的新样式设置默认参数。
styles.default_font.name = 'Courier New'
# 如果我们添加一个 "StyleType.Paragraph" 样式，集合将应用
# 其 "DefaultParagraphFormat" 属性的值到该样式的 "ParagraphFormat" 属性。
styles.default_paragraph_format.first_line_indent = 15
# 添加一个样式，然后验证它具有默认设置。
styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
self.assertEqual('Courier New', styles[4].font.name)
self.assertEqual(15, styles.get_by_name('MyStyle').paragraph_format.first_line_indent)
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

