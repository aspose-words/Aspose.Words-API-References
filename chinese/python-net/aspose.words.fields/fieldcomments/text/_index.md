---
title: FieldComments.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldComments.text property. Gets or sets the text of the comments."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldcomments/text/
---

## FieldComments.text property

Gets or sets the text of the comments.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to use the COMMENTS field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 为文档的 "Comments" 内置属性设置一个值。
doc.built_in_document_properties.comments = 'My comment.'
# 创建一个 COMMENTS 字段以显示该内置属性的值。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True).as_field_comments()
field.update()
self.assertEqual(' COMMENTS ', field.get_field_code())
self.assertEqual('My comment.', field.result)
# 如果我们为 COMMENTS 字段的 Text 属性赋值并更新它，字段将
# 用其 Text 属性的值覆盖 "Comments" 内置属性的当前值，
# 然后显示新的值。
field.text = 'My overriding comment.'
field.update()
self.assertEqual(' COMMENTS  "My overriding comment."', field.get_field_code())
self.assertEqual('My overriding comment.', field.result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.COMMENTS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldComments](../)

