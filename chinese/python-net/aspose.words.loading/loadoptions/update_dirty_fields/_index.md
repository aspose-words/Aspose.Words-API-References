---
title: LoadOptions.update_dirty_fields property
linktitle: update_dirty_fields property
articleTitle: update_dirty_fields property
second_title: Aspose.Words for Python
description: "LoadOptions.update_dirty_fields property. Specifies whether to update the fields with the ``dirty`` attribute."
type: docs
weight: 170
url: /zh/python-net/aspose.words.loading/loadoptions/update_dirty_fields/
---

## LoadOptions.update_dirty_fields property

Specifies whether to update the fields with the ``dirty`` attribute.



```python
@property
def update_dirty_fields(self) -> bool:
    ...

@update_dirty_fields.setter
def update_dirty_fields(self, value: bool):
    ...

```

### Examples

Shows how to use special property for updating field result.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 获取文档内置的 "Author" 属性值，然后使用字段显示它。
doc.built_in_document_properties.author = 'John Doe'
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
self.assertFalse(field.is_dirty)
self.assertEqual('John Doe', field.result)
# 更新属性。字段仍然显示旧值。
doc.built_in_document_properties.author = 'John & Jane Doe'
self.assertEqual('John Doe', field.result)
# 由于字段的值已过期，我们可以将其标记为 "dirty"。
# 此值将保持过期，直到我们使用 Field.Update() 方法手动更新字段。
field.is_dirty = True
with io.BytesIO() as doc_stream:
    # 如果我们在未调用更新方法的情况下保存，
    # 字段将在输出文档中继续显示过期的值。
    doc.save(stream=doc_stream, save_format=aw.SaveFormat.DOCX)
    # LoadOptions 对象具有更新所有字段的选项
    # 在加载文档时标记为 "dirty"。
    options = aw.loading.LoadOptions()
    options.update_dirty_fields = update_dirty_fields
    doc = aw.Document(stream=doc_stream, load_options=options)
    self.assertEqual('John & Jane Doe', doc.built_in_document_properties.author)
    field = doc.range.fields[0].as_field_author()
    # 像这样更新 dirty 字段会自动将它们的 "IsDirty" 标志设为 false。
    if update_dirty_fields:
        self.assertEqual('John & Jane Doe', field.result)
        self.assertFalse(field.is_dirty)
    else:
        self.assertEqual('John Doe', field.result)
        self.assertTrue(field.is_dirty)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

