---
title: SaveOptions.update_created_time_property property
linktitle: update_created_time_property property
articleTitle: update_created_time_property property
second_title: Aspose.Words for Python
description: "SaveOptions.update_created_time_property property. Gets or sets a value determining whether the [BuiltInDocumentProperties.created_time](../../../aspose.words.properties/builtindocumentproperties/created_time/) property is updated before saving"
type: docs
weight: 140
url: /it/python-net/aspose.words.saving/saveoptions/update_created_time_property/
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
# Questo flag determina se l'ora di creazione, che è una proprietà integrata, viene aggiornata.
# In tal caso, la data dell'ultima operazione di salvataggio del documento
# con questo oggetto SaveOptions passato come parametro è usata come ora di creazione.
save_options = aw.saving.DocSaveOptions()
save_options.update_created_time_property = is_update_created_time_property
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateCreatedTimeProperty.docx', save_options=save_options)
# Apri il documento salvato, quindi verifica il valore della proprietà.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateCreatedTimeProperty.docx')
if is_update_created_time_property:
    self.assertNotEqual(created_time, doc.built_in_document_properties.created_time)
else:
    self.assertEqual(created_time, doc.built_in_document_properties.created_time)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

