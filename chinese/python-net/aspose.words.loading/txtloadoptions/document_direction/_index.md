---
title: TxtLoadOptions.document_direction property
linktitle: document_direction property
articleTitle: document_direction property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.document_direction property. Gets or sets a document direction"
type: docs
weight: 50
url: /zh/python-net/aspose.words.loading/txtloadoptions/document_direction/
---

## TxtLoadOptions.document_direction property

Gets or sets a document direction.
The default value is [DocumentDirection.LEFT_TO_RIGHT](../../documentdirection/#LEFT_TO_RIGHT).



```python
@property
def document_direction(self) -> aspose.words.loading.DocumentDirection:
    ...

@document_direction.setter
def document_direction(self, value: aspose.words.loading.DocumentDirection):
    ...

```

### Examples

Shows how to detect plaintext document text direction.

```python
# 创建一个 "TxtLoadOptions" 对象，可将其传递给文档的构造函数
# 以修改加载纯文本文档的方式。
load_options = aw.loading.TxtLoadOptions()
# 将 "DocumentDirection" 属性设置为 "DocumentDirection.Auto"，可自动检测
# Aspose.Words 从纯文本加载的每个段落文本的方向。
# 每个段落的 "Bidi" 属性将存储其方向。
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# 将希伯来文检测为从右到左。
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# 将英文检测为从右到左。
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

