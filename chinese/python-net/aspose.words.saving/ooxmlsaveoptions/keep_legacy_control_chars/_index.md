---
title: OoxmlSaveOptions.keep_legacy_control_chars property
linktitle: keep_legacy_control_chars property
articleTitle: keep_legacy_control_chars property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.keep_legacy_control_chars property. Keeps original representation of legacy control characters."
type: docs
weight: 50
url: /zh/python-net/aspose.words.saving/ooxmlsaveoptions/keep_legacy_control_chars/
---

## OoxmlSaveOptions.keep_legacy_control_chars property

Keeps original representation of legacy control characters.


```python
@property
def keep_legacy_control_chars(self) -> bool:
    ...

@keep_legacy_control_chars.setter
def keep_legacy_control_chars(self, value: bool):
    ...

```

### Examples

Shows how to support legacy control characters when converting to .docx.

```python
doc = aw.Document(file_name=MY_DIR + 'Legacy control character.doc')
# 当我们将文档保存为 OOXML 格式时，可以创建一个 OoxmlSaveOptions 对象
# 然后将其传递给文档的保存方法，以修改文档的保存方式。
# 将 "KeepLegacyControlChars" 属性设置为 "true" 以保留
# 在保存时保留 "ShortDateTime" 旧版字符。
# 将 "KeepLegacyControlChars" 属性设置为 "false" 以移除
# 输出文档中的 "ShortDateTime" 旧版字符。
so = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
so.keep_legacy_control_chars = keep_legacy_control_chars
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.KeepLegacyControlChars.docx', save_options=so)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.KeepLegacyControlChars.docx')
self.assertEqual('\x13date \\@ "MM/dd/yyyy"\x14\x15\x0c' if keep_legacy_control_chars else '\x1e\x0c', doc.first_section.body.get_text())
```

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

