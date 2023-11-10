---
title: SaveOptions.update_last_printed_property property
linktitle: update_last_printed_property property
articleTitle: update_last_printed_property property
second_title: Aspose.Words for Python
description: "SaveOptions.update_last_printed_property property. Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving."
type: docs
weight: 150
url: /python-net/aspose.words.saving/saveoptions/update_last_printed_property/
---

## SaveOptions.update_last_printed_property property

Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving.



```python
@property
def update_last_printed_property(self) -> bool:
    ...

@update_last_printed_property.setter
def update_last_printed_property(self, value: bool):
    ...

```

### Examples

Shows how to update a document's "Last printed" property when saving.

```python
doc = aw.Document()

last_printed = datetime(2019, 12, 20, tzinfo=timezone.utc)
doc.built_in_document_properties.last_printed = last_printed

# This flag determines whether the last printed date, which is a built-in property, is updated.
# If so, then the date of the document's most recent save operation
# with this SaveOptions object passed as a parameter is used as the print date.
save_options = aw.saving.DocSaveOptions()
save_options.update_last_printed_property = is_update_last_printed_property

# In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
# It can also be displayed in the document's body by using a PRINTDATE field.
doc.save(ARTIFACTS_DIR + "DocSaveOptions.update_last_printed_property.doc", save_options)

# Open the saved document, then verify the value of the property.
doc = aw.Document(ARTIFACTS_DIR + "DocSaveOptions.update_last_printed_property.doc")

if is_update_last_printed_property:
    self.assertNotEqual(last_printed, doc.built_in_document_properties.last_printed)
else:
    self.assertEqual(last_printed, doc.built_in_document_properties.last_printed)
```

Shows how to update a document's "created_time" property when saving.

```python
doc = aw.Document()

created_time = datetime(2019, 12, 20, tzinfo=timezone.utc)
doc.built_in_document_properties.created_time = created_time

# This flag determines whether the created time, which is a built-in property, is updated.
# If so, then the date of the document's most recent save operation
# with this SaveOptions object passed as a parameter is used as the created time.
save_options = aw.saving.DocSaveOptions()
save_options.update_created_time_property = is_update_created_time_property

doc.save(ARTIFACTS_DIR + "DocSaveOptions.update_created_time_property.docx", save_options)

# Open the saved document, then verify the value of the property.
doc = aw.Document(ARTIFACTS_DIR + "DocSaveOptions.update_created_time_property.docx")

if is_update_created_time_property:
    self.assertNotEqual(created_time, doc.built_in_document_properties.created_time)
else:
    self.assertEqual(created_time, doc.built_in_document_properties.created_time)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

