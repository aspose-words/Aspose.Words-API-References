---
title: Field.is_dirty property
linktitle: is_dirty property
articleTitle: is_dirty property
second_title: Aspose.Words for Python
description: "Field.is_dirty property. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document."
type: docs
weight: 40
url: /python-net/aspose.words.fields/field/is_dirty/
---

## Field.is_dirty property

Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.


```python
@property
def is_dirty(self) -> bool:
    ...

@is_dirty.setter
def is_dirty(self, value: bool):
    ...

```

### Examples

Shows how to use special property for updating field result.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Give the document's built-in "author" property value, and then display it with a field.
doc.built_in_document_properties.author = "John Doe"
field = builder.insert_field(aw.fields.FieldType.FIELD_AUTHOR, True).as_field_author()

self.assertFalse(field.is_dirty)
self.assertEqual("John Doe", field.result)

# Update the property. The field still displays the old value.
doc.built_in_document_properties.author = "John & Jane Doe"

self.assertEqual("John Doe", field.result)

# Since the field's value is out of date, we can mark it as "dirty".
# This value will stay out of date until we update the field manually with the Field.update() method.
field.is_dirty = True

with io.BytesIO() as doc_stream:
    # If we save without calling an update method,
    # the field will keep displaying the out of date value in the output document.
    doc.save(doc_stream, aw.SaveFormat.DOCX)

    # The LoadOptions object has an option to update all fields
    # marked as "dirty" when loading the document.
    options = aw.loading.LoadOptions()
    options.update_dirty_fields = update_dirty_fields
    doc = aw.Document(doc_stream, options)

    self.assertEqual("John & Jane Doe", doc.built_in_document_properties.author)

    field = doc.range.fields[0].as_field_author()

    # Updating dirty fields like this automatically set their "is_dirty" flag to False.
    if update_dirty_fields:
        self.assertEqual("John & Jane Doe", field.result)
        self.assertFalse(field.is_dirty)
    else:
        self.assertEqual("John Doe", field.result)
        self.assertTrue(field.is_dirty)
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

