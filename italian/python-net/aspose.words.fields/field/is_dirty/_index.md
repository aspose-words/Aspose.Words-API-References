---
title: Field.is_dirty property
linktitle: is_dirty property
articleTitle: is_dirty property
second_title: Aspose.Words for Python
description: "Field.is_dirty property. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document."
type: docs
weight: 40
url: /it/python-net/aspose.words.fields/field/is_dirty/
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
builder = aw.DocumentBuilder(doc=doc)
# Fornisci il valore della proprietà integrata "Author" del documento, quindi visualizzalo con un campo.
doc.built_in_document_properties.author = 'John Doe'
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
self.assertFalse(field.is_dirty)
self.assertEqual('John Doe', field.result)
# Aggiorna la proprietà. Il campo visualizza ancora il valore precedente.
doc.built_in_document_properties.author = 'John & Jane Doe'
self.assertEqual('John Doe', field.result)
# Poiché il valore del campo è obsoleto, possiamo contrassegnarlo come "dirty".
# Questo valore rimarrà obsoleto finché non aggiorniamo manualmente il campo con il metodo Field.Update().
field.is_dirty = True
with io.BytesIO() as doc_stream:
    # Se salviamo senza chiamare un metodo di aggiornamento,
    # il campo continuerà a visualizzare il valore obsoleto nel documento di output.
    doc.save(stream=doc_stream, save_format=aw.SaveFormat.DOCX)
    # L'oggetto LoadOptions dispone di un'opzione per aggiornare tutti i campi
    # contrassegnati come "dirty" durante il caricamento del documento.
    options = aw.loading.LoadOptions()
    options.update_dirty_fields = update_dirty_fields
    doc = aw.Document(stream=doc_stream, load_options=options)
    self.assertEqual('John & Jane Doe', doc.built_in_document_properties.author)
    field = doc.range.fields[0].as_field_author()
    # Aggiornare i campi dirty in questo modo imposta automaticamente il loro flag "IsDirty" su false.
    if update_dirty_fields:
        self.assertEqual('John & Jane Doe', field.result)
        self.assertFalse(field.is_dirty)
    else:
        self.assertEqual('John Doe', field.result)
        self.assertTrue(field.is_dirty)
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

