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




### See Also

* module [aspose.words](../../)
* class [Document](../)
* class [CustomPart](../../../aspose.words.markup/custompart/)

