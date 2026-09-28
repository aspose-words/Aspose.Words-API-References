---
title: LoadOptions.update_dirty_fields property
linktitle: update_dirty_fields property
articleTitle: update_dirty_fields property
second_title: Aspose.Words for Python
description: "LoadOptions.update_dirty_fields property. Specifies whether to update the fields with the ``dirty`` attribute."
type: docs
weight: 170
url: /de/python-net/aspose.words.loading/loadoptions/update_dirty_fields/
---

## LoadOptions.update_dirty_fields property

Specifies whether to update the fields with the ``dirty`` attribute.



```python
@property
def update_dirty_fields(self) -> bool:
    ...

@update_dirty_fields.setter
def update_dirty_fields(self, value: bool):
    ...

```

### Examples

Shows how to use special property for updating field result.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Geben Sie den integrierten "Author"-Eigenschaftswert des Dokuments an und zeigen Sie ihn anschließend in einem Feld an.
doc.built_in_document_properties.author = 'John Doe'
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
self.assertFalse(field.is_dirty)
self.assertEqual('John Doe', field.result)
# Aktualisieren Sie die Eigenschaft. Das Feld zeigt immer noch den alten Wert an.
doc.built_in_document_properties.author = 'John & Jane Doe'
self.assertEqual('John Doe', field.result)
# Da der Wert des Feldes veraltet ist, können wir ihn als "dirty" markieren.
# Dieser Wert bleibt veraltet, bis wir das Feld manuell mit der Methode Field.Update() aktualisieren.
field.is_dirty = True
with io.BytesIO() as doc_stream:
    # Wenn wir speichern, ohne eine Aktualisierungsmethode aufzurufen,
    # wird das Feld den veralteten Wert im Ausgabedokument weiterhin anzeigen.
    doc.save(stream=doc_stream, save_format=aw.SaveFormat.DOCX)
    # Das LoadOptions-Objekt verfügt über eine Option, alle Felder zu aktualisieren
    # die beim Laden des Dokuments als "dirty" markiert werden.
    options = aw.loading.LoadOptions()
    options.update_dirty_fields = update_dirty_fields
    doc = aw.Document(stream=doc_stream, load_options=options)
    self.assertEqual('John & Jane Doe', doc.built_in_document_properties.author)
    field = doc.range.fields[0].as_field_author()
    # Das Aktualisieren von "dirty"-Feldern auf diese Weise setzt deren "IsDirty"-Flag automatisch auf false.
    if update_dirty_fields:
        self.assertEqual('John & Jane Doe', field.result)
        self.assertFalse(field.is_dirty)
    else:
        self.assertEqual('John Doe', field.result)
        self.assertTrue(field.is_dirty)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

