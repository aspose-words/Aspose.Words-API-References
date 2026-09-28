---
title: FieldSubject.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldSubject.text property. Gets or sets the text of the subject."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldsubject/text/
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
# Setzen Sie einen Wert für die integrierte Eigenschaft "Subject" des Dokuments.
doc.built_in_document_properties.subject = 'My subject'
# Erstellen Sie ein SUBJECT-Feld, um den Wert dieser integrierten Eigenschaft anzuzeigen.
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True).as_field_subject()
field.update()
self.assertEqual(' SUBJECT ', field.get_field_code())
self.assertEqual('My subject', field.result)
# Wenn wir dem Text-Eigenschaftswert des SUBJECT-Feldes einen Wert zuweisen und es aktualisieren, wird das Feld
# den aktuellen Wert der integrierten Eigenschaft "Subject" mit dem Wert seiner Text-Eigenschaft überschreiben,
# und anschließend den neuen Wert anzeigen.
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

