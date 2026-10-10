---
title: SaveOptions.update_last_printed_property property
linktitle: update_last_printed_property property
articleTitle: update_last_printed_property property
second_title: Aspose.Words for Python
description: "SaveOptions.update_last_printed_property property. Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving."
type: docs
weight: 160
url: /zh/python-net/aspose.words.saving/saveoptions/update_last_printed_property/
---

## SaveOptions.update_last_printed_property property

Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving.



```python
@property
def update_last_printed_property(self) -> bool:
    ...

@update_last_printed_property.setter
def update_last_printed_property(self, value: bool):
    ...

```

### Examples

Shows how to update a document's "Last printed" property when saving.

```python
doc = aw.Document()
last_printed = datetime.datetime(2019, 12, 20)
doc.built_in_document_properties.last_printed = last_printed
# 此标志决定是否更新最后打印日期（这是一个内置属性）。
# 如果是，则为文档最近一次保存操作的日期
# 使用此 SaveOptions 对象作为参数时，将其用作打印日期。
save_options = aw.saving.DocSaveOptions()
save_options.update_last_printed_property = is_update_last_printed_property
# 在 Microsoft Word 2003 中，可通过 文件 -> 属性 -> 统计信息 -> 已打印 来找到此属性。
# 它也可以通过使用 PRINTDATE 域在文档正文中显示。
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateLastPrintedProperty.doc', save_options=save_options)
# 打开已保存的文档，然后验证该属性的值。
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateLastPrintedProperty.doc')
if is_update_last_printed_property:
    self.assertNotEqual(last_printed, doc.built_in_document_properties.last_printed)
else:
    self.assertEqual(last_printed, doc.built_in_document_properties.last_printed)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

