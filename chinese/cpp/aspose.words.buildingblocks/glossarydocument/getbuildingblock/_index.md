---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock 方法"
linktitle: "GetBuildingBlock"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock 方法。使用指定的图库、类别和名称在 C++ 中查找构建块。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument::GetBuildingBlock method


使用指定的库、类别和名称查找构建块。

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock(Aspose::Words::BuildingBlocks::BuildingBlockGallery gallery, const System::String &category, const System::String &name)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 图库 | Aspose::Words::BuildingBlocks::BuildingBlockGallery | 画廊条件。 |
| 类别 | const System::String\& | 类别条件。可以是 **null**，在这种情况下它将不会用于比较。 |
| name | const System::String\& | 构建块名称条件。 |

### ReturnValue

匹配的构建块，若未找到匹配则为 **null**。
## 备注


这是一个便利方法，它遍历此集合中的所有构建块，并返回第一个匹配指定画廊、类别和名称的构建块。

Microsoft Word 将构建块组织到画廊中。画廊使用 [BuildingBlockGallery](../../buildingblockgallery/) 枚举预定义。在每个画廊内，构建块可以被组织到一个或多个类别中。类别名称是字符串。每个构建块都有一个名称。构建块名称不一定唯一。

## 另见

* Class [BuildingBlock](../../buildingblock/)
* Enum [BuildingBlockGallery](../../buildingblockgallery/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
