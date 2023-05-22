---
title: DocumentProperty.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for Python
description: "DocumentProperty.value property. Gets or sets the value of the property."
type: docs
weight: 50
url: /python-net/aspose.words.properties/documentproperty/value/
---

## DocumentProperty.value property

Gets or sets the value of the property.

Cannot be ``None``.




### Examples

Shows how to work with built-in document properties.

```python
doc = aw.Document(MY_DIR + "Properties.docx")

# The "Document" object contains some of its metadata in its members.
print(f"Document filename:\n\t \"{doc.original_file_name}\"")

# The document also stores metadata in its built-in properties.
# Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
print("Built-in Properties:")
for doc_property in doc.built_in_document_properties:
    print(doc_property.name)
    print(f"\tType:\t{doc_property.type}")

    # Some properties may store multiple values.
    if isinstance(doc_property.value, list):
        for value in doc_property.value:
            print(f"\tValue:\t\"{value}\"")
    else:
        print(f"\tValue:\t\"{doc_property.value}\"")
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

