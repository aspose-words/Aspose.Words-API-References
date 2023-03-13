﻿---
title: CustomPartCollection class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a collection of [CustomPart](../custompart/) objects"
type: docs
weight: 20
url: /python-net/aspose.words.markup/custompartcollection/
---

## CustomPartCollection class

Represents a collection of [CustomPart](../custompart/) objects.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




You do not normally need to create instances of this class. You access custom parts 
related to the OOXML package via the [Document.package_custom_parts](../../aspose.words/document/package_custom_parts/) property.




### Constructors
| Name | Description |
| --- | --- |
| [CustomPartCollection()](./__init__/#default) | The default constructor. |

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets an item at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(part)](./add/#custompart) | Adds an item to the collection. |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ clone()](./clone/#default) | Makes a deep copy of this collection and its items. |
|[ remove_at(index)](./remove_at/#int) | Removes an item at the specified index. |

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

* module [aspose.words.markup](../)
* class [CustomPart](../custompart/)
* property [Document.package_custom_parts](../../aspose.words/document/package_custom_parts/)

