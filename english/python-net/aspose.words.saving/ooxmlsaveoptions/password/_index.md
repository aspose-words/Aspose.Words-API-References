---
title: OoxmlSaveOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.password property. Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm."
type: docs
weight: 60
url: /python-net/aspose.words.saving/ooxmlsaveoptions/password/
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
builder = aw.DocumentBuilder(doc)
builder.writeln('Hello world!')
save_options = aw.saving.OoxmlSaveOptions()
save_options.password = 'MyPassword'
doc.save(ARTIFACTS_DIR + 'OoxmlSaveOptions.password.docx', save_options)
# We will not be able to open this document with Microsoft Word or
# Aspose.Words without providing the correct password.
with self.assertRaises(Exception):
    doc = aw.Document(ARTIFACTS_DIR + 'OoxmlSaveOptions.password.docx')
# Open the encrypted document by passing the correct password in a LoadOptions object.
doc = aw.Document(ARTIFACTS_DIR + 'OoxmlSaveOptions.password.docx', aw.loading.LoadOptions('MyPassword'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

