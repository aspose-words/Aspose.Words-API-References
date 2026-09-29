---
title: PropertyType enumeration
linktitle: PropertyType enumeration
articleTitle: PropertyType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.properties.PropertyType enumeration. Specifies data type of a document property."
type: docs
weight: 60
url: /it/python-net/aspose.words.properties/propertytype/
---

## PropertyType enumeration

Specifies data type of a document property.


### Members

| Name | Description |
| --- | --- |
| BOOLEAN | The property is a boolean value. |
| DATE_TIME | The property is a date time value. |
| DOUBLE | The property is a floating number. |
| NUMBER | The property is an integer number. |
| STRING | The property is a string value. |
| STRING_ARRAY | The property is an array of strings. |
| OBJECT_ARRAY | The property is an array of objects. |
| BYTE_ARRAY | The property is an array of bytes. |
| OTHER | The property is some other type. |

### Examples

Shows how to work with a document's custom properties.

```python
import datetime
import aspose.words as aw
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
doc = aw.Document()
properties = doc.custom_document_properties
self.assertEqual(0, properties.count)
# Le proprietà personalizzate del documento sono coppie chiave-valore che possiamo aggiungere al documento.
properties.add(name='Authorized', value=True)
properties.add(name='Authorized By', value='John Doe')
properties.add(name='Authorized Date', value=datetime.date.today())
properties.add(name='Authorized Revision', value=doc.built_in_document_properties.revision_number)
properties.add(name='Authorized Amount', value=123.45)
# La raccolta ordina le proprietà personalizzate in ordine alfabetico.
self.assertEqual(1, properties.index_of('Authorized Amount'))
self.assertEqual(5, properties.count)
# Stampa ogni proprietà personalizzata nel documento.
for prop in properties:
    print(f'Name: "{prop.name}"\n\tType: "{prop.type}"\n\tValue: "{prop.value}"')
# Visualizza il valore di una proprietà personalizzata usando un campo DOCPROPERTY.
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_code=' DOCPROPERTY "Authorized By"').as_field_doc_property()
field.update()
self.assertEqual('John Doe', field.result)
# Possiamo trovare queste proprietà personalizzate in Microsoft Word tramite "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.DocumentPropertyCollection.docx')
# Di seguito sono riportati tre modi per rimuovere le proprietà personalizzate da un documento.
# 1 -  Rimuovi per indice:
properties.remove_at(1)
self.assertFalse(properties.contains('Authorized Amount'))
self.assertEqual(4, properties.count)
# 2 -  Rimuovi per nome:
properties.remove('Authorized Revision')
self.assertFalse(properties.contains('Authorized Revision'))
self.assertEqual(3, properties.count)
# 3 -  Svuota l'intera raccolta in una volta:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.properties](../)
* class [DocumentProperty](../documentproperty/)
* property [DocumentProperty.type](../documentproperty/type/)

