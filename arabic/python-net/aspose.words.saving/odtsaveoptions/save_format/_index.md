---
title: OdtSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "OdtSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 60
url: /ar/python-net/aspose.words.saving/odtsaveoptions/save_format/
---

## OdtSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can be [SaveFormat.ODT](../../../aspose.words/saveformat/#ODT) or [SaveFormat.OTT](../../../aspose.words/saveformat/#OTT).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to encrypt a saved ODT/OTT document with a password, and then load it using Aspose.Words.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# أنشئ OdtSaveOptions جديدًا، ومرّر إما "SaveFormat.Odt"،
# أو "SaveFormat.Ott" كالصيغة لحفظ المستند بها.
save_options = aw.saving.OdtSaveOptions(save_format=save_format)
save_options.password = '@sposeEncrypted_1145'
extension_string = aw.FileFormatUtil.save_format_to_extension(save_format)
# إذا فتحنا هذا المستند باستخدام محرر مناسب،
# سوف يطلب منا كلمة المرور التي حددناها في كائن SaveOptions.
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string, save_options=save_options)
doc_info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string)
self.assertTrue(doc_info.is_encrypted)
# إذا رغبنا في فتح أو تعديل هذا المستند مرة أخرى باستخدام Aspose.Words،
# سيتعين علينا توفير كائن LoadOptions مع كلمة المرور الصحيحة إلى مُنشئ التحميل.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string, load_options=aw.loading.LoadOptions(password='@sposeEncrypted_1145'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [OdtSaveOptions](../)

