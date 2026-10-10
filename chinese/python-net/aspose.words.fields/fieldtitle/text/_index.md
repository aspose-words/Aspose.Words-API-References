---
title: FieldTitle.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldTitle.text property. Gets or sets the text of the title."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldtitle/text/
---

## FieldTitle.text property

Gets or sets the text of the title.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to use the TITLE field.

```python
doc = aw.Document()
# 为内置文档属性 \"Title\" 设置一个值。
doc.built_in_document_properties.title = 'My Title'
# 我们可以使用 TITLE 字段在文档中显示此属性的值。
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=False).as_field_title()
field.update()
self.assertEqual(' TITLE ', field.get_field_code())
self.assertEqual('My Title', field.result)
# 为字段的 Text 属性设置一个值，
# 然后更新字段也会用新值覆盖相应的内置属性。
builder.writeln()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=False).as_field_title()
field.text = 'My New Title'
field.update()
self.assertEqual(' TITLE  "My New Title"', field.get_field_code())
self.assertEqual('My New Title', field.result)
self.assertEqual('My New Title', doc.built_in_document_properties.title)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TITLE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldTitle](../)

