---
title: FieldTitle.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldTitle.text property. Gets or sets the text of the title."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldtitle/text/
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
# Set a value for the "Title" built-in document property.
doc.built_in_document_properties.title = 'My Title'
# We can use the TITLE field to display the value of this property in the document.
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=False).as_field_title()
field.update()
self.assertEqual(' TITLE ', field.get_field_code())
self.assertEqual('My Title', field.result)
# Setting a value for the field's Text property,
# and then updating the field will also overwrite the corresponding built-in property with the new value.
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

