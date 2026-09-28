---
title: FieldCreateDate.use_um_al_qura_calendar property
linktitle: use_um_al_qura_calendar property
articleTitle: use_um_al_qura_calendar property
second_title: Aspose.Words for Python
description: "FieldCreateDate.use_um_al_qura_calendar property. Gets or sets whether to use the Um-al-Qura calendar."
type: docs
weight: 40
url: /zh/python-net/aspose.words.fields/fieldcreatedate/use_um_al_qura_calendar/
---

## FieldCreateDate.use_um_al_qura_calendar property

Gets or sets whether to use the Um-al-Qura calendar.


```python
@property
def use_um_al_qura_calendar(self) -> bool:
    ...

@use_um_al_qura_calendar.setter
def use_um_al_qura_calendar(self, value: bool):
    ...

```

### Examples

Shows how to use the CREATEDATE field to display the creation date/time of the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.writeln(' Date this document was created:')
# 我们可以使用 CREATEDATE 字段来显示文档创建的日期和时间。
# 以下是三种不同的日历类型，CREATEDATE 字段可以根据它们显示日期/时间。
# 1 - 伊斯兰阴历：
builder.write('According to the Lunar Calendar - ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_CREATE_DATE, update_field=True).as_field_create_date()
field.use_lunar_calendar = True
assert ' CREATEDATE  \\h' == field.get_field_code()
# 2 - 乌姆阿尔库拉历：
builder.write('\nAccording to the Umm al-Qura Calendar - ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_CREATE_DATE, update_field=True).as_field_create_date()
field.use_um_al_qura_calendar = True
assert ' CREATEDATE  \\u' == field.get_field_code()
# 3 - 印度国家历：
builder.write('\nAccording to the Indian National Calendar - ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_CREATE_DATE, update_field=True).as_field_create_date()
field.use_saka_era_calendar = True
assert ' CREATEDATE  \\s' == field.get_field_code()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.CREATEDATE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCreateDate](../)

