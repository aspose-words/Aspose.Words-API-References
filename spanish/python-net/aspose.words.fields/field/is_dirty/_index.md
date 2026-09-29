---
title: Field.is_dirty property
linktitle: is_dirty property
articleTitle: is_dirty property
second_title: Aspose.Words for Python
description: "Field.is_dirty property. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document."
type: docs
weight: 40
url: /es/python-net/aspose.words.fields/field/is_dirty/
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
# Obtenga el valor de la propiedad incorporada "Author" del documento y luego muéstrelo con un campo.
doc.built_in_document_properties.author = 'John Doe'
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
self.assertFalse(field.is_dirty)
self.assertEqual('John Doe', field.result)
# Actualice la propiedad. El campo sigue mostrando el valor anterior.
doc.built_in_document_properties.author = 'John & Jane Doe'
self.assertEqual('John Doe', field.result)
# Dado que el valor del campo está desactualizado, podemos marcarlo como "dirty".
# Este valor permanecerá desactualizado hasta que actualicemos el campo manualmente con el método Field.Update().
field.is_dirty = True
with io.BytesIO() as doc_stream:
    # Si guardamos sin llamar a un método de actualización,
    # el campo seguirá mostrando el valor desactualizado en el documento de salida.
    doc.save(stream=doc_stream, save_format=aw.SaveFormat.DOCX)
    # El objeto LoadOptions tiene una opción para actualizar todos los campos
    # marcados como "dirty" al cargar el documento.
    options = aw.loading.LoadOptions()
    options.update_dirty_fields = update_dirty_fields
    doc = aw.Document(stream=doc_stream, load_options=options)
    self.assertEqual('John & Jane Doe', doc.built_in_document_properties.author)
    field = doc.range.fields[0].as_field_author()
    # Actualizar campos dirty de esta manera establece automáticamente su bandera "IsDirty" a false.
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

