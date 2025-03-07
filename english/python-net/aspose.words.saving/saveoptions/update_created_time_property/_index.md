---
title: SaveOptions.update_created_time_property property
linktitle: update_created_time_property property
articleTitle: update_created_time_property property
second_title: Aspose.Words for Python
description: "SaveOptions.update_created_time_property property. Gets or sets a value determining whether the [BuiltInDocumentProperties.created_time](../../../aspose.words.properties/builtindocumentproperties/created_time/) property is updated before saving"
type: docs
weight: 140
url: /python-net/aspose.words.saving/saveoptions/update_created_time_property/
---

## SaveOptions.update_created_time_property property

Gets or sets a value determining whether the [BuiltInDocumentProperties.created_time](../../../aspose.words.properties/builtindocumentproperties/created_time/) property is updated before saving.
Default value is ``False``;



```python
@property
def update_created_time_property(self) -> bool:
    ...

@update_created_time_property.setter
def update_created_time_property(self, value: bool):
    ...

```

### Examples

Shows how to update a document's "CreatedTime" property when saving.

```python
doc = aw.Document()
created_time = datetime.datetime(2019, 12, 20)
doc.built_in_document_properties.created_time = created_time
# This flag determines whether the created time, which is a built-in property, is updated.
# If so, then the date of the document's most recent save operation
# with this SaveOptions object passed as a parameter is used as the created time.
save_options = aw.saving.DocSaveOptions()
save_options.update_created_time_property = is_update_created_time_property
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateCreatedTimeProperty.docx', save_options=save_options)
# Open the saved document, then verify the value of the property.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateCreatedTimeProperty.docx')
if is_update_created_time_property:
    self.assertNotEqual(created_time, doc.built_in_document_properties.created_time)
else:
    self.assertEqual(created_time, doc.built_in_document_properties.created_time)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

