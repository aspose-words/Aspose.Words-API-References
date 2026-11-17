---
title: Aspose::Words::BuildingBlocks::BuildingBlock::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::BuildingBlock::Accept method. Accepts a visitor in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::BuildingBlocks::BuildingBlock::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

Calls [VisitBuildingBlockStart()](../../../aspose.words/documentvisitor/visitbuildingblockstart/), then calls [Accept()](../../../aspose.words/node/accept/) for all child nodes of this building block, then calls [VisitBuildingBlockEnd()](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Note: A building block node and its children are not visited when you execute a Visitor over a [Document](../../../aspose.words/document/). If you want to execute a Visitor over a building block, you need to execute the visitor over [GlossaryDocument](../../glossarydocument/) or call [Accept()](./).

## See Also

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
