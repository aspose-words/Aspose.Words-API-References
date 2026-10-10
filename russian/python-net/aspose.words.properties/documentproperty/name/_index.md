---
title: DocumentProperty.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "DocumentProperty.name property. Returns the name of the property."
type: docs
weight: 30
url: /ru/python-net/aspose.words.properties/documentproperty/name/
---

## DocumentProperty.name property

Returns the name of the property.


```python
@property
def name(self) -> str:
    ...

```

### Remarks

Cannot be ``None`` and cannot be an empty string.




### Examples

Shows how to work with built-in document properties.

```python
doc = aw.Document(file_name=MY_DIR + 'Properties.docx')
# Объект "Document" содержит часть своей метаданных в своих членах.
print(f'Document filename:\n\t "{doc.original_file_name}"')
# Документ также сохраняет метаданные во встроенных свойствах.
# Каждое встроенное свойство является членом объекта "BuiltInDocumentProperties" документа.
print('Built-in Properties:')
for doc_property in doc.built_in_document_properties:
    print(doc_property.name)
    print(f'\tType:\t{doc_property.type}')
    # Некоторые свойства могут хранить несколько значений.
    if isinstance(doc_property.value, (list, tuple)):
        for value in doc_property.value:
            print(f'\tValue:\t"{value}"')
    else:
        print(f'\tValue:\t"{doc_property.value}"')
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

