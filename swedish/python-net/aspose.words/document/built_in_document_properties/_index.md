---
title: Document.built_in_document_properties property
linktitle: built_in_document_properties property
articleTitle: built_in_document_properties property
second_title: Aspose.Words for Python
description: "Document.built_in_document_properties property. Returns a collection that represents all the built-in document properties of the document."
type: docs
weight: 50
url: /sv/python-net/aspose.words/document/built_in_document_properties/
---

## Document.built_in_document_properties property

Returns a collection that represents all the built-in document properties of the document.


```python
@property
def built_in_document_properties(self) -> aspose.words.properties.BuiltInDocumentProperties:
    ...

```

### Examples

Shows how to work with built-in document properties.

```python
doc = aw.Document(file_name=MY_DIR + 'Properties.docx')
# "Document"-objektet innehåller en del av dess metadata i sina medlemmar.
print(f'Document filename:\n\t "{doc.original_file_name}"')
# Dokumentet lagrar också metadata i sina inbyggda egenskaper.
# Varje inbyggd egenskap är en medlem i dokumentets "BuiltInDocumentProperties"-objekt.
print('Built-in Properties:')
for doc_property in doc.built_in_document_properties:
    print(doc_property.name)
    print(f'\tType:\t{doc_property.type}')
    # Vissa egenskaper kan lagra flera värden.
    if isinstance(doc_property.value, (list, tuple)):
        for value in doc_property.value:
            print(f'\tValue:\t"{value}"')
    else:
        print(f'\tValue:\t"{doc_property.value}"')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

