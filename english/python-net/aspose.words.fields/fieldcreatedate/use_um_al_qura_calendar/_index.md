---
title: FieldCreateDate.use_um_al_qura_calendar property
linktitle: use_um_al_qura_calendar property
articleTitle: use_um_al_qura_calendar property
second_title: Aspose.Words for Python
description: "FieldCreateDate.use_um_al_qura_calendar property. Gets or sets whether to use the Um-al-Qura calendar."
type: docs
weight: 40
url: /python-net/aspose.words.fields/fieldcreatedate/use_um_al_qura_calendar/
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
doc = aw.Document(MY_DIR + "Document.docx")
builder = aw.DocumentBuilder(doc)
builder.move_to_document_end()
builder.writeln(" Date this document was created:")

# We can use the CREATEDATE field to display the date and time of the creation of the document.
# Below are three different calendar types according to which the CREATEDATE field can display the date/time.
# 1 -  Islamic Lunar Calendar:
builder.write("According to the Lunar Calendar - ")
field = builder.insert_field(aw.fields.FieldType.FIELD_CREATE_DATE, True).as_field_create_date()
field.use_lunar_calendar = True

self.assertEqual(" CREATEDATE  \\h", field.get_field_code())

# 2 -  Umm al-Qura calendar:
builder.write("\nAccording to the Umm al-Qura Calendar - ")
field = builder.insert_field(aw.fields.FieldType.FIELD_CREATE_DATE, True).as_field_create_date()
field.use_um_al_qura_calendar = True

self.assertEqual(" CREATEDATE  \\u", field.get_field_code())

# 3 -  Indian National Calendar:
builder.write("\nAccording to the Indian National Calendar - ")
field = builder.insert_field(aw.fields.FieldType.FIELD_CREATE_DATE, True).as_field_create_date()
field.use_saka_era_calendar = True

self.assertEqual(" CREATEDATE  \\s", field.get_field_code())

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_create_date.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCreateDate](../)

