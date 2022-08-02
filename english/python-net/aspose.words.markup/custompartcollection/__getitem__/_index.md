---
title: CustomPartCollection indexer
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets an item at the specified index."
type: docs
weight: 20
url: /python-net/aspose.words.markup/custompartcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets or sets an item at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to access a document's arbitrary custom parts collection.

```python
doc = aw.Document(MY_DIR + "Custom parts OOXML package.docx")

self.assertEqual(2, doc.package_custom_parts.count)

# Clone the second part, then add the clone to the collection.
cloned_part = doc.package_custom_parts[1].clone()
doc.package_custom_parts.add(cloned_part)

self.assertEqual(3, doc.package_custom_parts.count)

# Enumerate over the collection and print every part.
for index, part in enumerate(doc.package_custom_parts):
    print(f"Part index {index}:")
    print(f"\tName:\t\t\t\t{part.name}")
    print(f"\tContent type:\t\t{part.content_type}")
    print(f"\tRelationship type:\t{part.relationship_type}")
    if part.is_external:
        print("\tSourced from outside the document")
    else:
        print(f"\tStored within the document, length: {len(part.data)} bytes")

# We can remove elements from this collection individually, or all at once.
doc.package_custom_parts.remove_at(2)

self.assertEqual(2, doc.package_custom_parts.count)

doc.package_custom_parts.clear()

self.assertEqual(0, doc.package_custom_parts.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomPartCollection](../)

