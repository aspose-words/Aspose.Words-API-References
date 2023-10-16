---
title: CustomPart class
linktitle: CustomPart class
articleTitle: CustomPart class
second_title: Aspose.Words for Python
description: "aspose.words.markup.CustomPart class. Represents a custom (arbitrary content) part, that is not defined by the ISO/IEC 29500 standard"
type: docs
weight: 10
url: /python-net/aspose.words.markup/custompart/
---

## CustomPart class

Represents a custom (arbitrary content) part, that is not defined by the ISO/IEC 29500 standard.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




This class represents an OOXML part that is a target of an "unknown relationship".
All relationships not defined within ISO/IEC 29500 are considered "unknown relationships".
Unknown relationships are permitted within an Office Open XML document provided that they 
conform to relationship markup guidelines.

Microsoft Word preserves custom parts during open/save cycles. Some additional info can be found 
here http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words also roundtrips custom parts and in addition, allows to programmatically access 
such parts via the [CustomPart](./) and [CustomPartCollection](../custompartcollection/) objects.

Do not confuse custom parts with Custom XML Data. Use [CustomXmlPart](../customxmlpart/) if you need 
to access Custom XML Data.




### Constructors
| Name | Description |
| --- | --- |
| [CustomPart()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [content_type](./content_type/) | Specifies the content type of this custom part. |
| [data](./data/) | Contains the data of this custom part. |
| [is_external](./is_external/) | False if this custom part is stored inside the OOXML package. True if this custom part is an external target. |
| [name](./name/) | Gets or sets this part's absolute name within the OOXML package or the target URL. |
| [relationship_type](./relationship_type/) | Gets or sets the relationship type from the parent part to this custom part. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Makes a "deep enough" copy of the object.  Does not duplicate the bytes of the [CustomPart.data](./data/) value. |

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
* class [CustomPartCollection](../custompartcollection/)
* property [Document.package_custom_parts](../../aspose.words/document/package_custom_parts/)

