---
title: DocSaveOptions constructor
linktitle: DocSaveOptions constructor
articleTitle: DocSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.DocSaveOptions constructor"
type: docs
weight: 10
url: /zh/python-net/aspose.words.saving/docsaveoptions/__init__/
---

## DocSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOC](../../../aspose.words/saveformat/#DOC) format.



```python
def __init__(self):
    ...
```

## DocSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOC](../../../aspose.words/saveformat/#DOC) or
[SaveFormat.DOT](../../../aspose.words/saveformat/#DOT) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Can be [SaveFormat.DOC](../../../aspose.words/saveformat/#DOC) or [SaveFormat.DOT](../../../aspose.words/saveformat/#DOT). |

## Examples

Shows how to set save options for older Microsoft Word formats.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Hello world!')
options = aw.saving.DocSaveOptions(aw.SaveFormat.DOC)
# 设置密码以保护文档被 Microsoft Word 或 Aspose.Words 加载。
# 请注意，这并不会以任何方式加密文档内容。
options.password = 'MyPassword'
# 如果文档包含流转单，我们可以在保存时通过将此标志设为 true 来保留它。
options.save_routing_slip = True
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', save_options=options)
# 为了能够加载文档，
# 我们需要在 LoadOptions 对象中应用我们在 DocSaveOptions 对象中指定的密码。
with self.assertRaises(Exception):
    doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc')
load_options = aw.loading.LoadOptions(password='MyPassword')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', load_options=load_options)
self.assertEqual('Hello world!', doc.get_text().strip())
```

## See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

