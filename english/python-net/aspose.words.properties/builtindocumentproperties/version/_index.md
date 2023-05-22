---
title: BuiltInDocumentProperties.version property
linktitle: version property
articleTitle: version property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.version property. Represents the version number of the application that created the document."
type: docs
weight: 320
url: /python-net/aspose.words.properties/builtindocumentproperties/version/
---

## BuiltInDocumentProperties.version property

Represents the version number of the application that created the document.

When a document was created by Microsoft Word, then high 16 bit represent
the major version and low 16 bit represent the build number.




### Examples

Shows how to work with document properties in the "Origin" category.

```python
# Open a document that we have created and edited using Microsoft Word.
doc = aw.Document(MY_DIR + "Properties.docx")
properties = doc.built_in_document_properties

# The following built-in properties contain information regarding the creation and editing of this document.
# We can right-click this document in Windows Explorer and find
# these properties via "Properties" -> "Details" -> "Origin" category.
# Fields such as PRINTDATE and EDITTIME can display these values in the document body.
print(f"Created using {properties.name_of_application}, on {properties.created_time}")
print("Minutes spent editing:", properties.total_editing_time)
print("Date/time last printed:", properties.last_printed)
print("Template document:", properties.template)

# We can also change the values of built-in properties.
properties.company = "Doe Ltd."
properties.manager = "Jane Doe"
properties.version = 5
properties.revision_number += 1

# Microsoft Word updates the following properties automatically when we save the document.
# To use these properties with Aspose.Words, we will need to set values for them manually.
properties.last_saved_by = "John Doe"
properties.last_saved_time = datetime.utcnow()

# We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
doc.save(ARTIFACTS_DIR + "DocumentProperties.origin.docx")
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

