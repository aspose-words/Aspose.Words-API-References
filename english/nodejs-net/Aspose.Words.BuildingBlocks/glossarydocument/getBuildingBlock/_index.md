---
title: GlossaryDocument.getBuildingBlock method
linktitle: getBuildingBlock method
articleTitle: getBuildingBlock method
second_title: Aspose.Words for NodeJs
description: "GlossaryDocument.getBuildingBlock method. Finds a building block using the specified gallery, category and name."
type: docs
weight: 90
url: /nodejs-net/aspose.words.buildingblocks/glossarydocument/getBuildingBlock/
---

## getBuildingBlock(gallery, category, name) {#buildingblockgallery_string_string}

Finds a building block using the specified gallery, category and name.


```js
getBuildingBlock(gallery: Aspose.Words.BuildingBlocks.BuildingBlockGallery, category: string, name: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| gallery | [BuildingBlockGallery](../../buildingblockgallery/) | The gallery criteria. |
| category | string | The category criteria. Can be ``null``, in which case it will not be used for comparison. |
| name | string | The building block name criteria. |

### Remarks

This is a convenience method that iterates over all building blocks
in this collection and returns the first building block that matches
the specified gallery, category and name.

Microsoft Word organizes building blocks into galleries. The galleries
are predefined using the [BuildingBlockGallery](../../buildingblockgallery/) enum.
Within each gallery, building blocks can be organized into one or more categories.
The category name is a string. Each building block has a name. A building block
name is not guaranteed to be unique.




### Returns

The matching building block or ``null`` if a match was not found.


### See Also

* module [Aspose.Words.BuildingBlocks](../../)
* class [GlossaryDocument](../)

