---
title: OoxmlSaveOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.password property. Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm."
type: docs
weight: 60
url: /es/python-net/aspose.words.saving/ooxmlsaveoptions/password/
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
# No podremos abrir este documento con Microsoft Word o
# Aspose.Words sin proporcionar la contraseña correcta.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Password.docx')
# Abra el documento cifrado pasando la contraseña correcta en un objeto LoadOptions.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Password.docx', load_options=aw.loading.LoadOptions(password='MyPassword'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

