---
title: FieldOptions.default_document_author property
linktitle: default_document_author property
articleTitle: default_document_author property
second_title: Aspose.Words for Python
description: "FieldOptions.default_document_author property. Gets or sets default document author's name"
type: docs
weight: 60
url: /python-net/aspose.words.fields/fieldoptions/default_document_author/
---

## FieldOptions.default_document_author property

Gets or sets default document author's name. If author's name is already specified in built-in document properties,
this option is not considered.


### Examples

Shows how to use an AUTHOR field to display a document creator's name.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# AUTHOR fields source their results from the built-in document property called "author".
# If we create and save a document in Microsoft Word,
# it will have our username in that property.
# However, if we create a document programmatically using Aspose.Words,
# the "author" property, by default, will be an empty string.
self.assertEqual("", doc.built_in_document_properties.author)

# Set a backup author name for AUTHOR fields to use
# if the "author" property contains an empty string.
doc.field_options.default_document_author = "Joe Bloggs"

builder.write("This document was created by ")
field = builder.insert_field(aw.fields.FieldType.FIELD_AUTHOR, True).as_field_author()
field.update()

self.assertEqual(" AUTHOR ", field.get_field_code())
self.assertEqual("Joe Bloggs", field.result)

# Updating an AUTHOR field that contains a value
# will apply that value to the "author" built-in property.
self.assertEqual("Joe Bloggs", doc.built_in_document_properties.author)

# Changing this property, then updating the AUTHOR field will apply this value to the field.
doc.built_in_document_properties.author = "John Doe"
field.update()

self.assertEqual(" AUTHOR ", field.get_field_code())
self.assertEqual("John Doe", field.result)

# If we update an AUTHOR field after changing its "name" property,
# then the field will display the new name and apply the new name to the built-in property.
field.author_name = "Jane Doe"
field.update()

self.assertEqual(" AUTHOR  \"Jane Doe\"", field.get_field_code())
self.assertEqual("Jane Doe", field.result)

# AUTHOR fields do not affect the "default_document_author" property.
self.assertEqual("Jane Doe", doc.built_in_document_properties.author)
self.assertEqual("Joe Bloggs", doc.field_options.default_document_author)

doc.save(ARTIFACTS_DIR + "Field.field_author.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

