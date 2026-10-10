---
title: DocumentPropertyCollection indexer
linktitle: DocumentPropertyCollection indexer
articleTitle: DocumentPropertyCollection indexer
second_title: Aspose.Words for Python
description: "DocumentPropertyCollection indexer. Returns a [DocumentProperty](../../documentproperty/) object by index."
type: docs
weight: 10
url: /tr/python-net/aspose.words.properties/documentpropertycollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Returns a [DocumentProperty](../../documentproperty/) object by index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to work with custom document properties.

```python
doc = aw.Document(MY_DIR + 'Properties.docx')
# Her belge, yerleşik özellikler gibi anahtar-değer çiftleri olan bir özel özellik koleksiyonu içerir.
# Belgenin sabit bir yerleşik özellik listesi vardır. Kullanıcı tüm özel özellikleri oluşturur.
self.assertEqual('Value of custom document property', str(doc.custom_document_properties.get_by_name('CustomProperty')))
doc.custom_document_properties.add('CustomProperty2', 'Value of custom document property #2')
print('Custom Properties:')
for custom_document_property in doc.custom_document_properties:
    print(custom_document_property.name)
    print(f'\tType:\t{custom_document_property.type}')
    print(f'\tValue:\t"{custom_document_property.value}"')
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentPropertyCollection](../)

