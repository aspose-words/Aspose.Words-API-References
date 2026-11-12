---
title: FieldInfo.info_type property
linktitle: info_type property
articleTitle: info_type property
second_title: Aspose.Words for Python
description: "FieldInfo.info_type property. Gets or sets the type of the document property to insert."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fieldinfo/info_type/
---

## FieldInfo.info_type property

Gets or sets the type of the document property to insert.


```python
@property
def info_type(self) -> str:
    ...

@info_type.setter
def info_type(self, value: str):
    ...

```

### Examples

Shows how to work with INFO fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# "Comments" yerleşik özelliği için bir değer ayarlayın ve ardından o özelliğin değerini göstermek için bir INFO alanı ekleyin.
doc.built_in_document_properties.comments = 'My comment'
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INFO, update_field=True).as_field_info()
field.info_type = 'Comments'
field.update()
self.assertEqual(' INFO  Comments', field.get_field_code())
self.assertEqual('My comment', field.result)
builder.writeln()
# Alan'ın NewValue özelliği için bir değer ayarlama ve güncelleme
# alan, aynı zamanda karşılık gelen yerleşik özelliği yeni değerle üzerine yazacaktır.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INFO, update_field=True).as_field_info()
field.info_type = 'Comments'
field.new_value = 'New comment'
field.update()
self.assertEqual(' INFO  Comments "New comment"', field.get_field_code())
self.assertEqual('New comment', field.result)
self.assertEqual('New comment', doc.built_in_document_properties.comments)
doc.save(file_name=ARTIFACTS_DIR + 'Field.INFO.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldInfo](../)

