---
title: TxtSaveOptionsBase.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.encoding property. Specifies the encoding to use when exporting in text formats"
type: docs
weight: 10
url: /zh/python-net/aspose.words.saving/txtsaveoptionsbase/encoding/
---

## TxtSaveOptionsBase.encoding property

Specifies the encoding to use when exporting in text formats. 
Default value is **Encoding.UTF8**.



```python
@property
def encoding(self) -> str:
    ...

@encoding.setter
def encoding(self, value: str):
    ...

```

### Examples

Shows how to set encoding for a .txt output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 添加一些包含 ASCII 字符集之外字符的文本。
builder.write('À È Ì Ò Ù.')
# 创建一个 "TxtSaveOptions" 对象，我们可以将其传递给文档的 "Save" 方法
# 以修改我们将文档保存为纯文本的方式。
txt_save_options = aw.saving.TxtSaveOptions()
# 验证 "Encoding" 属性是否包含适用于我们文档内容的相应编码。
self.assertEqual(system_helper.text.Encoding.utf_8(), txt_save_options.encoding)
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.UTF8.txt', save_options=txt_save_options)
doc_text = system_helper.text.Encoding.get_string(system_helper.io.File.read_all_bytes(ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.UTF8.txt'), system_helper.text.Encoding.utf_8())
self.assertEqual('\ufeffÀ È Ì Ò Ù.\r\n', doc_text)
# 使用不合适的编码可能导致文档内容丢失。
txt_save_options.encoding = system_helper.text.Encoding.ascii()
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.ASCII.txt', save_options=txt_save_options)
doc_text = system_helper.text.Encoding.get_string(system_helper.io.File.read_all_bytes(ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.ASCII.txt'), system_helper.text.Encoding.ascii())
self.assertEqual('? ? ? ? ?.\r\n', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

