---
title: FieldOptions.default_document_author property
linktitle: default_document_author property
articleTitle: default_document_author property
second_title: Aspose.Words for Python
description: "FieldOptions.default_document_author property. Gets or sets default document author's name"
type: docs
weight: 70
url: /es/python-net/aspose.words.fields/fieldoptions/default_document_author/
---

## FieldOptions.default_document_author property

Gets or sets default document author's name. If author's name is already specified in built-in document properties,
this option is not considered.


```python
@property
def default_document_author(self) -> str:
    ...

@default_document_author.setter
def default_document_author(self, value: str):
    ...

```

### Examples

Shows how to use an AUTHOR field to display a document creator's name.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Los campos AUTHOR obtienen sus resultados de la propiedad de documento incorporada llamada "Author".
# Si creamos y guardamos un documento en Microsoft Word,
# tendrá nuestro nombre de usuario en esa propiedad.
# Sin embargo, si creamos un documento programáticamente usando Aspose.Words,
# la propiedad "Author", por defecto, será una cadena vacía.
self.assertEqual('', doc.built_in_document_properties.author)
# Establezca un nombre de autor de respaldo para que los campos AUTHOR lo usen
# si la propiedad "Author" contiene una cadena vacía.
doc.field_options.default_document_author = 'Joe Bloggs'
builder.write('This document was created by ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('Joe Bloggs', field.result)
# Actualizar un campo AUTHOR que contiene un valor
# aplicará ese valor a la propiedad incorporada "Author".
self.assertEqual('Joe Bloggs', doc.built_in_document_properties.author)
# Cambiar esta propiedad, y luego actualizar el campo AUTHOR aplicará este valor al campo.
doc.built_in_document_properties.author = 'John Doe'
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('John Doe', field.result)
# Si actualizamos un campo AUTHOR después de cambiar su propiedad "Name",
# entonces el campo mostrará el nuevo nombre y aplicará el nuevo nombre a la propiedad incorporada.
field.author_name = 'Jane Doe'
field.update()
self.assertEqual(' AUTHOR  "Jane Doe"', field.get_field_code())
self.assertEqual('Jane Doe', field.result)
# Los campos AUTHOR no afectan la propiedad DefaultDocumentAuthor.
self.assertEqual('Jane Doe', doc.built_in_document_properties.author)
self.assertEqual('Joe Bloggs', doc.field_options.default_document_author)
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTHOR.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

