---
title: SaveOptions.update_last_printed_property property
linktitle: update_last_printed_property property
articleTitle: update_last_printed_property property
second_title: Aspose.Words for Python
description: "SaveOptions.update_last_printed_property property. Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving."
type: docs
weight: 160
url: /de/python-net/aspose.words.saving/saveoptions/update_last_printed_property/
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
last_printed = datetime.datetime(2019, 12, 20)
doc.built_in_document_properties.last_printed = last_printed
# Dieses Flag bestimmt, ob das zuletzt gedruckte Datum, das eine integrierte Eigenschaft ist, aktualisiert wird.
# Falls ja, dann das Datum des letzten Speichervorgangs des Dokuments
# wird mit diesem SaveOptions‑Objekt, das als Parameter übergeben wird, als Druckdatum verwendet.
save_options = aw.saving.DocSaveOptions()
save_options.update_last_printed_property = is_update_last_printed_property
# In Microsoft Word 2003 kann diese Eigenschaft über Datei -> Eigenschaften -> Statistik -> Gedruckt gefunden werden.
# Sie kann auch im Dokumentenkörper angezeigt werden, indem ein PRINTDATE‑Feld verwendet wird.
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateLastPrintedProperty.doc', save_options=save_options)
# Öffnen Sie das gespeicherte Dokument und überprüfen Sie anschließend den Wert der Eigenschaft.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateLastPrintedProperty.doc')
if is_update_last_printed_property:
    self.assertNotEqual(last_printed, doc.built_in_document_properties.last_printed)
else:
    self.assertEqual(last_printed, doc.built_in_document_properties.last_printed)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

