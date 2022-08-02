---
title: get_building_block method
second_title: Aspose.Words for Python via .NET API Reference
description: "Finds a building block using the specified gallery, category and name."
type: docs
weight: 70
url: /python-net/aspose.words.buildingblocks/glossarydocument/get_building_block/
---

## get_building_block(gallery, category, name) {#buildingblockgallery_str_str}

Finds a building block using the specified gallery, category and name.


```python
def get_building_block(self, gallery: aspose.words.buildingblocks.BuildingBlockGallery, category: str, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| gallery | [BuildingBlockGallery](../../buildingblockgallery/) |  |
| category | str |  |
| name | str |  |

This is a convenience method that iterates over all building blocks
in this collection and returns the first building block that matches
the specified gallery, category and name.

Microsoft Word organizes building blocks into galleries. The galleries
are predefined using the [BuildingBlockGallery](../../buildingblockgallery/) enum.
Within each gallery, building blocks can be organized into one or more categories.
The category name is a string. Each building block has a name. A building block
name is not guaranteed to be unique.




### Returns

The matching building block or null if a match was not found.


### See Also

* module [aspose.words.buildingblocks](../../)
* class [GlossaryDocument](../)

