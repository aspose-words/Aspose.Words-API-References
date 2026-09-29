---
title: Document.custom_document_properties property
linktitle: custom_document_properties property
articleTitle: custom_document_properties property
second_title: Aspose.Words for Python
description: "Document.custom_document_properties property. Returns a collection that represents all the custom document properties of the document."
type: docs
weight: 80
url: /ru/python-net/aspose.words/document/custom_document_properties/
---

## Document.custom_document_properties property

Returns a collection that represents all the custom document properties of the document.


```python
@property
def custom_document_properties(self) -> aspose.words.properties.CustomDocumentProperties:
    ...

```

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

* module [aspose.words](../../)
* class [Document](../)

