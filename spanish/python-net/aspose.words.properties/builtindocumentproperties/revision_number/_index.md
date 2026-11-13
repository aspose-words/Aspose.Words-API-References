---
title: BuiltInDocumentProperties.revision_number property
linktitle: revision_number property
articleTitle: revision_number property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.revision_number property. Gets or sets the document revision number."
type: docs
weight: 250
url: /es/python-net/aspose.words.properties/builtindocumentproperties/revision_number/
---

## BuiltInDocumentProperties.revision_number property

Gets or sets the document revision number.


```python
@property
def revision_number(self) -> int:
    ...

@revision_number.setter
def revision_number(self, value: int):
    ...

```

### Remarks

Aspose.Words does not update this property.




### Examples

Shows how to work with REVNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Current revision #')
# Inserte un campo REVNUM, que muestra la propiedad del número de revisión actual del documento.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REVISION_NUM, update_field=True).as_field_rev_num()
self.assertEqual(' REVNUM ', field.get_field_code())
self.assertEqual('1', field.result)
self.assertEqual(1, doc.built_in_document_properties.revision_number)
# Esta propiedad cuenta cuántas veces se ha guardado un documento en Microsoft Word,
# y no está relacionada con las revisiones rastreadas. Podemos encontrarla haciendo clic derecho en el documento en el Explorador de Windows
# a través de Propiedades -> Detalles. Podemos actualizar esta propiedad manualmente.
doc.built_in_document_properties.revision_number += 1
field.update()
self.assertEqual('2', field.result)
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

