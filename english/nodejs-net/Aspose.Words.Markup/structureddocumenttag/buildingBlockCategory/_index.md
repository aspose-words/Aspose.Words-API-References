---
title: StructuredDocumentTag.buildingBlockCategory property
linktitle: buildingBlockCategory property
articleTitle: buildingBlockCategory property
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTag.buildingBlockCategory property. Specifies category of building block for this SDT node"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttag/buildingBlockCategory/
---

## StructuredDocumentTag.buildingBlockCategory property

Specifies category of building block for this **SDT** node.
Can not be ``None``.



```js
get buildingBlockCategory(): string
```

### Remarks

Accessing this property will only work for [SdtType.BuildingBlockGallery](../../sdttype/#BuildingBlockGallery) and
[SdtType.DocPartObj](../../sdttype/#DocPartObj) SDT types. It is read-only for **SDT** of the document part type.


For all other SDT types exception will occur.




### Examples

Shows how to insert a structured document tag as a building block, and set its category and gallery.

```js
let doc = new aw.Document();

let buildingBlockSdt = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.BuildingBlockGallery, aw.Markup.MarkupLevel.Block);
buildingBlockSdt.buildingBlockCategory = "Built-in";
buildingBlockSdt.buildingBlockGallery = "Table of Contents";

doc.firstSection.body.appendChild(buildingBlockSdt);

doc.save(base.artifactsDir + "StructuredDocumentTag.BuildingBlockCategories.docx");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

