---
title: DocumentProperty.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for Python
description: "DocumentProperty.value property. Gets or sets the value of the property."
type: docs
weight: 50
url: /it/python-net/aspose.words.properties/documentproperty/value/
---

## DocumentProperty.value property

Gets or sets the value of the property.


```python
@property
def value(self) -> object:
    ...

@value.setter
def value(self, value: object):
    ...

```

### Remarks

Cannot be ``None``.




### Examples

Shows how to work with built-in document properties.

```python
doc = aw.Document(file_name=MY_DIR + 'Properties.docx')
# L'oggetto "Document" contiene parte dei suoi metadati nei suoi membri.
print(f'Document filename:\n\t "{doc.original_file_name}"')
# Il documento memorizza inoltre i metadati nelle sue proprietà incorporate.
# Ogni proprietà incorporata è un membro dell'oggetto "BuiltInDocumentProperties" del documento.
print('Built-in Properties:')
for doc_property in doc.built_in_document_properties:
    print(doc_property.name)
    print(f'\tType:\t{doc_property.type}')
    # Alcune proprietà possono memorizzare più valori.
    if isinstance(doc_property.value, (list, tuple)):
        for value in doc_property.value:
            print(f'\tValue:\t"{value}"')
    else:
        print(f'\tValue:\t"{doc_property.value}"')
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

