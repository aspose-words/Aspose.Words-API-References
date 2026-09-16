---
title: "Aspose::Words::BuildingBlocks::BuildingBlock::Accept 方法"
linktitle: "Accept"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BuildingBlocks::BuildingBlock::Accept 方法。接受 C++ 中的访问者。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock::Accept method


接受访问者。

```cpp
bool Aspose::Words::BuildingBlocks::BuildingBlock::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 访问者 | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | 将访问这些节点的访问者。 |

### ReturnValue

如果所有节点都已被访问则为 True；如果 [DocumentVisitor](../../../aspose.words/documentvisitor/) 在访问所有节点之前停止了操作则为 false。
## 备注


遍历此节点及其所有子节点。每个节点都会调用 [DocumentVisitor](../../../aspose.words/documentvisitor/) 上的相应方法。

更多信息请参阅 Visitor 设计模式。

调用 [VisitBuildingBlockStart()](../../../aspose.words/documentvisitor/visitbuildingblockstart/)，然后为此构建块的所有子节点调用 [Accept()](../../../aspose.words/node/accept/)，最后调用 [VisitBuildingBlockEnd()](../../../aspose.words/documentvisitor/visitbuildingblockend/)。

注意：当您对 [Document](../../../aspose.words/document/) 执行 Visitor 时，构建块节点及其子节点不会被访问。如果想对构建块执行 Visitor，需要对 [GlossaryDocument](../../glossarydocument/) 执行该 Visitor，或调用 [Accept()](./)。

## 另见

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
