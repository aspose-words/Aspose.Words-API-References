---
title: Document.packageCustomParts property
linktitle: packageCustomParts property
articleTitle: packageCustomParts property
second_title: Aspose.Words for NodeJs
description: "Document.packageCustomParts property. Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using unknown relationships."
type: docs
weight: 300
url: /nodejs-net/Aspose.Words/document/packageCustomParts/
---

## Document.packageCustomParts property

Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".


```js
get packageCustomParts(): Aspose.Words.Markup.CustomPartCollection
```

### Remarks

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts,
use the [Document.customXmlParts](../customXmlParts/) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship".
For more information see [CustomPart](../../../aspose.words.markup/custompart/).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be ``None``.




### See Also

* module [Aspose.Words](../../)
* class [Document](../)
* class [CustomPart](../../../aspose.words.markup/custompart/)

