---
title: LoadOptions constructor
linktitle: LoadOptions constructor
articleTitle: LoadOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.loading.LoadOptions constructor"
type: docs
weight: 10
url: /zh/python-net/aspose.words.loading/loadoptions/__init__/
---

## LoadOptions() {#default}

Initializes a new instance of this class with default values.


```python
def __init__(self):
    ...
```

## LoadOptions(password) {#str}

A shortcut to initialize a new instance of this class with the specified password to load an encrypted document.


```python
def __init__(self, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | str | The password to open an encrypted document. Can be ``None`` or empty string. |

## LoadOptions(load_format, password, base_uri) {#loadformat_str_str}

A shortcut to initialize a new instance of this class with properties set to the specified values.


```python
def __init__(self, load_format: aspose.words.LoadFormat, password: str, base_uri: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| load_format | [LoadFormat](../../../aspose.words/loadformat/) | The format of the document to be loaded. |
| password | str | The password to open an encrypted document. Can be ``None`` or empty string. |
| base_uri | str | The string that will be used to resolve relative URIs to absolute. Can be ``None`` or empty string. |

## Examples

Shows how to load an encrypted Microsoft Word document.

```python
doc = None
# 如果尝试在没有密码的情况下打开加密文档，Aspose.Words 会抛出异常。
with self.assertRaises(Exception):
    doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx')
# 加载此类文档时，密码通过 LoadOptions 对象传递给文档的构造函数。
options = aw.loading.LoadOptions(password='docPassword')
# 使用 LoadOptions 对象加载加密文档有两种方式。
# 1 -  通过文件名从本地文件系统加载文档：
doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx', load_options=options)
# 2 -  从流中加载文档：
with system_helper.io.File.open_read(MY_DIR + 'Encrypted.docx') as stream:
    doc = aw.Document(stream=stream, load_options=options)
```

Shows how to specify a base URI when opening an html document.

```python
# 假设我们想加载一个包含相对 URI 链接图像的 .html 文档
# 而图像位于不同的位置。在这种情况下，我们需要将相对 URI 解析为绝对 URI。
# 我们可以使用 HtmlLoadOptions 对象提供基准 URI。
load_options = aw.loading.HtmlLoadOptions(load_format=aw.LoadFormat.HTML, password='', base_uri=IMAGE_DIR)
self.assertEqual(aw.LoadFormat.HTML, load_options.load_format)
doc = aw.Document(file_name=MY_DIR + 'Missing image.html', load_options=load_options)
# 虽然输入的 .html 中图像损坏，但我们的自定义基准 URI 帮助我们修复了链接。
image_shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
self.assertTrue(image_shape.is_image)
# 此输出文档将显示缺失的图像。
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.BaseUri.docx')
```

## See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

