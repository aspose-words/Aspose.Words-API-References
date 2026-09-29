---
title: FieldSubject.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldSubject.text property. Gets or sets the text of the subject."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldsubject/text/
---

## FieldSubject.text property

Gets or sets the text of the subject.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to use the SUBJECT field.

```python
doc = aw.Document()
# Ange ett värde för dokumentets inbyggda egenskap \"Subject\".
doc.built_in_document_properties.subject = 'My subject'
# Skapa ett SUBJECT-fält för att visa värdet av den inbyggda egenskapen.
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True).as_field_subject()
field.update()
self.assertEqual(' SUBJECT ', field.get_field_code())
self.assertEqual('My subject', field.result)
# Om vi ger SUBJECT-fältets Text-egenskap ett värde och uppdaterar det, kommer fältet att
# skriva över det aktuella värdet för den inbyggda egenskapen \"Subject\" med värdet från dess Text-egenskap,
# och sedan visa det nya värdet.
field.text = 'My new subject'
field.update()
self.assertEqual(' SUBJECT  "My new subject"', field.get_field_code())
self.assertEqual('My new subject', field.result)
self.assertEqual('My new subject', doc.built_in_document_properties.subject)
doc.save(file_name=ARTIFACTS_DIR + 'Field.SUBJECT.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSubject](../)

