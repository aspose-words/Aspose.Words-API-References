---
title: SaveOptions.update_last_printed_property property
linktitle: update_last_printed_property property
articleTitle: update_last_printed_property property
second_title: Aspose.Words for Python
description: "SaveOptions.update_last_printed_property property. Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving."
type: docs
weight: 160
url: /es/python-net/aspose.words.saving/saveoptions/update_last_printed_property/
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
# Esta bandera determina si la fecha de última impresión, que es una propiedad incorporada, se actualiza.
# Si es así, entonces la fecha de la operación de guardado más reciente del documento
# con este objeto SaveOptions pasado como parámetro se usa como la fecha de impresión.
save_options = aw.saving.DocSaveOptions()
save_options.update_last_printed_property = is_update_last_printed_property
# En Microsoft Word 2003, esta propiedad se puede encontrar a través de Archivo -> Propiedades -> Estadísticas -> Impreso.
# También puede mostrarse en el cuerpo del documento usando un campo PRINTDATE.
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateLastPrintedProperty.doc', save_options=save_options)
# Abra el documento guardado, luego verifique el valor de la propiedad.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.UpdateLastPrintedProperty.doc')
if is_update_last_printed_property:
    self.assertNotEqual(last_printed, doc.built_in_document_properties.last_printed)
else:
    self.assertEqual(last_printed, doc.built_in_document_properties.last_printed)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

