---
title: OdtSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "OdtSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 60
url: /zh/python-net/aspose.words.saving/odtsaveoptions/save_format/
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
# 创建一个新的 OdtSaveOptions，并传入 "SaveFormat.Odt"，
# 或 "SaveFormat.Ott" 作为文档的保存格式。
save_options = aw.saving.OdtSaveOptions(save_format=save_format)
save_options.password = '@sposeEncrypted_1145'
extension_string = aw.FileFormatUtil.save_format_to_extension(save_format)
# 如果我们使用合适的编辑器打开此文档，
# 它会提示我们输入在 SaveOptions 对象中指定的密码。
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string, save_options=save_options)
doc_info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string)
self.assertTrue(doc_info.is_encrypted)
# 如果我们希望再次使用 Aspose.Words 打开或编辑此文档，
# 我们必须向加载构造函数提供一个包含正确密码的 LoadOptions 对象。
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string, load_options=aw.loading.LoadOptions(password='@sposeEncrypted_1145'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [OdtSaveOptions](../)

