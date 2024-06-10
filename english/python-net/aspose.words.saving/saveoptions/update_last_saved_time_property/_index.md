---
title: SaveOptions.update_last_saved_time_property property
linktitle: update_last_saved_time_property property
articleTitle: update_last_saved_time_property property
second_title: Aspose.Words for Python
description: "SaveOptions.update_last_saved_time_property property. Gets or sets a value determining whether the [BuiltInDocumentProperties.last_saved_time](../../../aspose.words.properties/builtindocumentproperties/last_saved_time/) property is updated before saving."
type: docs
weight: 160
url: /python-net/aspose.words.saving/saveoptions/update_last_saved_time_property/
---

## SaveOptions.update_last_saved_time_property property

Gets or sets a value determining whether the [BuiltInDocumentProperties.last_saved_time](../../../aspose.words.properties/builtindocumentproperties/last_saved_time/) property is updated before saving.



```python
@property
def update_last_saved_time_property(self) -> bool:
    ...

@update_last_saved_time_property.setter
def update_last_saved_time_property(self, value: bool):
    ...

```

### Examples

Shows how to determine whether to preserve the document's "Last saved time" property when saving.

```python
doc = aw.Document(MY_DIR + 'Document.docx')
self.assertEqual(datetime.datetime(2021, 5, 11, 6, 32, 0, tzinfo=datetime.timezone.utc), doc.built_in_document_properties.last_saved_time)
# When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
# and then pass it to the document's saving method to modify how we save the document.
# Set the "update_last_saved_time_property" property to "True" to
# set the output document's "Last saved time" built-in property to the current date/time.
# Set the "update_last_saved_time_property" property to "False" to
# preserve the original value of the input document's "Last saved time" built-in property.
save_options = aw.saving.OoxmlSaveOptions()
save_options.update_last_saved_time_property = update_last_saved_time_property
doc.save(ARTIFACTS_DIR + 'OoxmlSaveOptions.last_saved_time.docx', save_options)
doc = aw.Document(ARTIFACTS_DIR + 'OoxmlSaveOptions.last_saved_time.docx')
last_saved_time_new = doc.built_in_document_properties.last_saved_time
if update_last_saved_time_property:
    self.assertAlmostEqual(datetime.datetime.now(datetime.timezone.utc), last_saved_time_new, delta=datetime.timedelta(days=1))
else:
    self.assertEqual(datetime.datetime(2021, 5, 11, 6, 32, 0, tzinfo=datetime.timezone.utc), last_saved_time_new)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

