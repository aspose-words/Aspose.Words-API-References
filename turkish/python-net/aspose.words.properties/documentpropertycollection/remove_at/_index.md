---
title: DocumentPropertyCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "DocumentPropertyCollection.remove_at method. Removes a property at the specified index."
type: docs
weight: 80
url: /tr/python-net/aspose.words.properties/documentpropertycollection/remove_at/
---

## remove_at(index) {#int}

Removes a property at the specified index.


```python
def remove_at(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### Examples

Shows how to work with a document's custom properties.

```python
import datetime
import aspose.words as aw
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
doc = aw.Document()
properties = doc.custom_document_properties
self.assertEqual(0, properties.count)
# Özel belge özellikleri, belgeye ekleyebileceğimiz anahtar-değer çiftleridir.
properties.add(name='Authorized', value=True)
properties.add(name='Authorized By', value='John Doe')
properties.add(name='Authorized Date', value=datetime.date.today())
properties.add(name='Authorized Revision', value=doc.built_in_document_properties.revision_number)
properties.add(name='Authorized Amount', value=123.45)
# Koleksiyon, özel özellikleri alfabetik sıraya göre sıralar.
self.assertEqual(1, properties.index_of('Authorized Amount'))
self.assertEqual(5, properties.count)
# Belgedeki tüm özel özellikleri yazdır.
for prop in properties:
    print(f'Name: "{prop.name}"\n\tType: "{prop.type}"\n\tValue: "{prop.value}"')
# Bir DOCPROPERTY alanı kullanarak bir özel özelliğin değerini göster.
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_code=' DOCPROPERTY "Authorized By"').as_field_doc_property()
field.update()
self.assertEqual('John Doe', field.result)
# Bu özel özellikleri Microsoft Word'de "File" -> "Properties" > "Advanced Properties" > "Custom" yoluyla bulabiliriz.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.DocumentPropertyCollection.docx')
# Aşağıda, bir belgeden özel özellikleri kaldırmanın üç yolu bulunmaktadır.
# 1 -  İndeks ile kaldır:
properties.remove_at(1)
self.assertFalse(properties.contains('Authorized Amount'))
self.assertEqual(4, properties.count)
# 2 -  İsimle kaldır:
properties.remove('Authorized Revision')
self.assertFalse(properties.contains('Authorized Revision'))
self.assertEqual(3, properties.count)
# 3 -  Tüm koleksiyonu bir kerede boşalt:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentPropertyCollection](../)

