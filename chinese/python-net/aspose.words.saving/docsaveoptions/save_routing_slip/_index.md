---
title: DocSaveOptions.save_routing_slip property
linktitle: save_routing_slip property
articleTitle: save_routing_slip property
second_title: Aspose.Words for Python
description: "DocSaveOptions.save_routing_slip property. When ``False``, RoutingSlip data is not saved to output document"
type: docs
weight: 70
url: /zh/python-net/aspose.words.saving/docsaveoptions/save_routing_slip/
---

## DocSaveOptions.save_routing_slip property

When ``False``, RoutingSlip data is not saved to output document.
Default value is ``True``.



```python
@property
def save_routing_slip(self) -> bool:
    ...

@save_routing_slip.setter
def save_routing_slip(self, value: bool):
    ...

```

### Examples

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

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

