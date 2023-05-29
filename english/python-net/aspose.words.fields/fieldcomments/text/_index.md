---
title: FieldComments.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldComments.text property. Gets or sets the text of the comments."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldcomments/text/
---

## FieldComments.text property

Gets or sets the text of the comments.


### Examples

Shows how to use the COMMENTS field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Set a value for the document's "comments" built-in property.
doc.built_in_document_properties.comments = "My comment."

# Create a COMMENTS field to display the value of that built-in property.
field = builder.insert_field(aw.fields.FieldType.FIELD_COMMENTS, True).as_field_comments()
field.update()

self.assertEqual(" COMMENTS ", field.get_field_code())
self.assertEqual("My comment.", field.result)

# If we give the COMMENTS field's Text property value and update it, the field will
# overwrite the current value of the "comments" built-in property with the value of its Text property,
# and then display the new value.
field.text = "My overriding comment."
field.update()

self.assertEqual(" COMMENTS  \"My overriding comment.\"", field.get_field_code())
self.assertEqual("My overriding comment.", field.result)

doc.save(ARTIFACTS_DIR + "Field.field_comments.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldComments](../)

