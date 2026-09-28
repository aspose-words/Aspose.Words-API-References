---
title: DocSaveOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for Python
description: "DocSaveOptions.password property. Gets/sets a password to encrypt document using RC4 encryption method."
type: docs
weight: 40
url: /zh/python-net/aspose.words.saving/docsaveoptions/password/
---

## DocSaveOptions.password property

Gets/sets a password to encrypt document using RC4 encryption method.


```python
@property
def password(self) -> str:
    ...

@password.setter
def password(self, value: str):
    ...

```

### Remarks

In order to save document without encryption this property should be ``None`` or empty string.




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

