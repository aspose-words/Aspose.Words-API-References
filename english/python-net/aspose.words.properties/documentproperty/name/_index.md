---
title: name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns the name of the property."
type: docs
weight: 30
url: /python-net/aspose.words.properties/documentproperty/name/
---

## DocumentProperty.name property

Returns the name of the property.

Cannot be ``None`` and cannot be an empty string.




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

