---
title: "Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd 方法"
linktitle: "VisitBuildingBlockEnd"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd 方法。 当在 C++ 中枚举构建块结束时调用。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/documentvisitor/visitbuildingblockend/
---
## DocumentVisitor::VisitBuildingBlockEnd method


当构建块的枚举结束时调用。

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 块 | System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\> | 正在被访问的对象。 |

### ReturnValue

一个指定如何继续枚举的 [VisitorAction](../../visitoraction/) 值。
## 备注


注意：当您对 [Document](../../document/) 执行 Visitor 时，构建块节点及其子节点不会被访问。如果您想对构建块执行 Visitor，需要对 [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) 执行该 Visitor，或调用 [Accept()](../../../aspose.words.buildingblocks/buildingblock/accept/)。

## 另见

* Enum [VisitorAction](../../visitoraction/)
* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
