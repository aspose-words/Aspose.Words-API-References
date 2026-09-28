---
title: OoxmlSaveOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.password property. Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm."
type: docs
weight: 60
url: /zh/python-net/aspose.words.saving/ooxmlsaveoptions/password/
---

## OoxmlSaveOptions.password property

Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm.


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

Shows how to create a password encrypted Office Open XML document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
save_options = aw.saving.OoxmlSaveOptions()
save_options.password = 'MyPassword'
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Password.docx', save_options=save_options)
# 我们将无法使用 Microsoft Word 或
# Aspose.Words 打开此文档，除非提供正确的密码。
with self.assertRaises(Exception):
    doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Password.docx')
# 通过在 LoadOptions 对象中传递正确的密码来打开加密文档。
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Password.docx', load_options=aw.loading.LoadOptions(password='MyPassword'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

