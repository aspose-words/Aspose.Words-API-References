---
title: DocumentPropertyCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "DocumentPropertyCollection.count property. Gets number of items in the collection."
type: docs
weight: 20
url: /ru/python-net/aspose.words.properties/documentpropertycollection/count/
---

## DocumentPropertyCollection.count property

Gets number of items in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to work with custom document properties.

```python
doc = aw.Document(MY_DIR + 'Properties.docx')
# Каждый документ содержит коллекцию пользовательских свойств, которые, как и встроенные свойства, представляют собой пары «ключ‑значение».
# Документ имеет фиксированный список встроенных свойств. Пользователь создаёт все пользовательские свойства.
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

