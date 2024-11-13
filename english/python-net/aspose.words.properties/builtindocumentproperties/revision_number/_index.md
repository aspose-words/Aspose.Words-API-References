---
title: BuiltInDocumentProperties.revision_number property
linktitle: revision_number property
articleTitle: revision_number property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.revision_number property. Gets or sets the document revision number."
type: docs
weight: 250
url: /python-net/aspose.words.properties/builtindocumentproperties/revision_number/
---

## BuiltInDocumentProperties.revision_number property

Gets or sets the document revision number.


```python
@property
def revision_number(self) -> int:
    ...

@revision_number.setter
def revision_number(self, value: int):
    ...

```

### Remarks

Aspose.Words does not update this property.




### Examples

Shows how to work with document properties in the "Origin" category.

```python
# Open a document that we have created and edited using Microsoft Word.
doc = aw.Document(file_name=MY_DIR + 'Properties.docx')
properties = doc.built_in_document_properties
# The following built-in properties contain information regarding the creation and editing of this document.
# We can right-click this document in Windows Explorer and find
# these properties via "Properties" -> "Details" -> "Origin" category.
# Fields such as PRINTDATE and EDITTIME can display these values in the document body.
print(f'Created using {properties.name_of_application}, on {properties.created_time}')
print(f'Minutes spent editing: {properties.total_editing_time}')
print(f'Date/time last printed: {properties.last_printed}')
print(f'Template document: {properties.template}')
# We can also change the values of built-in properties.
properties.company = 'Doe Ltd.'
properties.manager = 'Jane Doe'
properties.version = 5
properties.revision_number += 1
# Microsoft Word updates the following properties automatically when we save the document.
# To use these properties with Aspose.Words, we will need to set values for them manually.
properties.last_saved_by = 'John Doe'
properties.last_saved_time = datetime.datetime.now()
# We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Origin.docx')
```

Shows how to work with REVNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Current revision #')
# Insert a REVNUM field, which displays the document's current revision number property.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REVISION_NUM, update_field=True).as_field_rev_num()
self.assertEqual(' REVNUM ', field.get_field_code())
self.assertEqual('1', field.result)
self.assertEqual(1, doc.built_in_document_properties.revision_number)
# This property counts how many times a document has been saved in Microsoft Word,
# and is unrelated to tracked revisions. We can find it by right clicking the document in Windows Explorer
# via Properties -> Details. We can update this property manually.
doc.built_in_document_properties.revision_number += 1
field.update()
self.assertEqual('2', field.result)
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

