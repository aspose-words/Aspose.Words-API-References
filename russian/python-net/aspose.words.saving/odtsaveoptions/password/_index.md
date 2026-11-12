---
title: OdtSaveOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for Python
description: "OdtSaveOptions.password property. Gets or sets a password to encrypt document."
type: docs
weight: 50
url: /ru/python-net/aspose.words.saving/odtsaveoptions/password/
---

## OdtSaveOptions.password property

Gets or sets a password to encrypt document.


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

Shows how to encrypt a saved ODT/OTT document with a password, and then load it using Aspose.Words.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Создайте новый OdtSaveOptions и передайте либо "SaveFormat.Odt",
# либо "SaveFormat.Ott" в качестве формата для сохранения документа.
save_options = aw.saving.OdtSaveOptions(save_format=save_format)
save_options.password = '@sposeEncrypted_1145'
extension_string = aw.FileFormatUtil.save_format_to_extension(save_format)
# Если мы откроем этот документ в соответствующем редакторе,
# он запросит у нас пароль, указанный в объекте SaveOptions.
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string, save_options=save_options)
doc_info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string)
self.assertTrue(doc_info.is_encrypted)
# Если мы захотим снова открыть или отредактировать этот документ с помощью Aspose.Words,
# нам придётся предоставить объект LoadOptions с правильным паролем конструктору загрузки.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string, load_options=aw.loading.LoadOptions(password='@sposeEncrypted_1145'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [OdtSaveOptions](../)

