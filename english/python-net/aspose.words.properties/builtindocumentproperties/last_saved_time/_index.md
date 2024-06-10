---
title: BuiltInDocumentProperties.last_saved_time property
linktitle: last_saved_time property
articleTitle: last_saved_time property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.last_saved_time property. Gets or sets the time of the last save in UTC."
type: docs
weight: 170
url: /python-net/aspose.words.properties/builtindocumentproperties/last_saved_time/
---

## BuiltInDocumentProperties.last_saved_time property

Gets or sets the time of the last save in UTC.


```python
@property
def last_saved_time(self) -> datetime.datetime:
    ...

@last_saved_time.setter
def last_saved_time(self, value: datetime.datetime):
    ...

```

### Remarks

For documents originated from RTF format this property returns the local time of last save operation.

Aspose.Words does not update this property.




### Examples

Shows how to work with document properties in the "Origin" category.

```python
# Open a document that we have created and edited using Microsoft Word.
doc = aw.Document(MY_DIR + 'Properties.docx')
properties = doc.built_in_document_properties
# The following built-in properties contain information regarding the creation and editing of this document.
# We can right-click this document in Windows Explorer and find
# these properties via "Properties" -> "Details" -> "Origin" category.
# Fields such as PRINTDATE and EDITTIME can display these values in the document body.
print(f'Created using {properties.name_of_application}, on {properties.created_time}')
print('Minutes spent editing:', properties.total_editing_time)
print('Date/time last printed:', properties.last_printed)
print('Template document:', properties.template)
# We can also change the values of built-in properties.
properties.company = 'Doe Ltd.'
properties.manager = 'Jane Doe'
properties.version = 5
properties.revision_number += 1
# Microsoft Word updates the following properties automatically when we save the document.
# To use these properties with Aspose.Words, we will need to set values for them manually.
properties.last_saved_by = 'John Doe'
properties.last_saved_time = datetime.utcnow()
# We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
doc.save(ARTIFACTS_DIR + 'DocumentProperties.origin.docx')
```

Shows how to use the SAVEDATE field to display the date/time of the document's most recent save operation performed using Microsoft Word.

```python
doc = aw.Document(MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc)
builder.move_to_document_end()
builder.writeln(' Date this document was last saved:')
# We can use the SAVEDATE field to display the last save operation's date and time on the document.
# The save operation that these fields refer to is the manual save in an application like Microsoft Word,
# not the document's "save" method.
# Below are three different calendar types according to which the SAVEDATE field can display the date/time.
# 1 -  Islamic Lunar Calendar:
builder.write('According to the Lunar Calendar - ')
field = builder.insert_field(aw.fields.FieldType.FIELD_SAVE_DATE, True).as_field_save_date()
field.use_lunar_calendar = True
self.assertEqual(' SAVEDATE  \\h', field.get_field_code())
# 2 -  Umm al-Qura calendar:
builder.write('\nAccording to the Umm al-Qura calendar - ')
field = builder.insert_field(aw.fields.FieldType.FIELD_SAVE_DATE, True).as_field_save_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' SAVEDATE  \\u', field.get_field_code())
# 3 -  Indian National calendar:
builder.write('\nAccording to the Indian National calendar - ')
field = builder.insert_field(aw.fields.FieldType.FIELD_SAVE_DATE, True).as_field_save_date()
field.use_saka_era_calendar = True
self.assertEqual(' SAVEDATE  \\s', field.get_field_code())
# The SAVEDATE fields draw their date/time values from the "last_saved_time" built-in property.
# The document's Save method will not update this value, but we can still update it manually.
doc.built_in_document_properties.last_saved_time = datetime.now()
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.field_save_date.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

