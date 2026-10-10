---
title: FieldSubject.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldSubject.text property. Gets or sets the text of the subject."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fieldsubject/text/
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
# Belgenin "Subject" yerleşik özelliği için bir değer ayarlayın.
doc.built_in_document_properties.subject = 'My subject'
# Bu yerleşik özelliğin değerini göstermek için bir SUBJECT alanı oluşturun.
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True).as_field_subject()
field.update()
self.assertEqual(' SUBJECT ', field.get_field_code())
self.assertEqual('My subject', field.result)
# Eğer SUBJECT alanının Text özelliğine bir değer verir ve güncellerseniz, alan
# "Subject" yerleşik özelliğinin mevcut değerini, Text özelliğinin değeriyle üzerine yazar,
# ve ardından yeni değeri gösterir.
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

