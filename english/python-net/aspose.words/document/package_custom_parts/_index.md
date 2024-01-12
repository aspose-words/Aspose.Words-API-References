---
title: Document.package_custom_parts property
linktitle: package_custom_parts property
articleTitle: package_custom_parts property
second_title: Aspose.Words for Python
description: "Document.package_custom_parts property. Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using unknown relationships."
type: docs
weight: 320
url: /python-net/aspose.words/document/package_custom_parts/
---

## Document.package_custom_parts property

Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".


```python
@property
def package_custom_parts(self) -> aspose.words.markup.CustomPartCollection:
    ...

@package_custom_parts.setter
def package_custom_parts(self, value: aspose.words.markup.CustomPartCollection):
    ...

```

### Remarks

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts,
use the [Document.custom_xml_parts](../custom_xml_parts/) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship".
For more information see [CustomPart](../../../aspose.words.markup/custompart/).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be ``None``.




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

* module [aspose.words](../../)
* class [Document](../)
* class [CustomPart](../../../aspose.words.markup/custompart/)

