---
title: Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock method
linktitle: GetBuildingBlock
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock method. Finds a building block using the specified gallery, category and name in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument::GetBuildingBlock method


Finds a building block using the specified gallery, category and name.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock(Aspose::Words::BuildingBlocks::BuildingBlockGallery gallery, const System::String &category, const System::String &name)
```


| Parameter | Type | Description |
| --- | --- | --- |
| gallery | Aspose::Words::BuildingBlocks::BuildingBlockGallery | The gallery criteria. |
| category | const System::String\& | The category criteria. Can be **null**, in which case it will not be used for comparison. |
| name | const System::String\& | The building block name criteria. |

### ReturnValue

The matching building block or **null** if a match was not found.
## Remarks


This is a convenience method that iterates over all building blocks in this collection and returns the first building block that matches the specified gallery, category and name.

Microsoft Word organizes building blocks into galleries. The galleries are predefined using the [BuildingBlockGallery](../../buildingblockgallery/) enum. Within each gallery, building blocks can be organized into one or more categories. The category name is a string. Each building block has a name. A building block name is not guaranteed to be unique.

## See Also

* Class [BuildingBlock](../../buildingblock/)
* Enum [BuildingBlockGallery](../../buildingblockgallery/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
