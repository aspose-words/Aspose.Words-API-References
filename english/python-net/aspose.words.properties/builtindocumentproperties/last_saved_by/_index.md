﻿---
title: BuiltInDocumentProperties.last_saved_by property
linktitle: last_saved_by property
articleTitle: last_saved_by property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.last_saved_by property. Gets or sets the name of the last author."
type: docs
weight: 170
url: /python-net/aspose.words.properties/builtindocumentproperties/last_saved_by/
---

## BuiltInDocumentProperties.last_saved_by property

Gets or sets the name of the last author.


```python
@property
def last_saved_by(self) -> str:
    ...

@last_saved_by.setter
def last_saved_by(self, value: str):
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

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

