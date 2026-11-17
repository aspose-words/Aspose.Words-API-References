---
title: Aspose::Words::DocumentVisitor::VisitBuildingBlockStart method
linktitle: VisitBuildingBlockStart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentVisitor::VisitBuildingBlockStart method. Called when enumeration of a building block has started in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words/documentvisitor/visitbuildingblockstart/
---
## DocumentVisitor::VisitBuildingBlockStart method


Called when enumeration of a building block has started.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockStart(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
```


| Parameter | Type | Description |
| --- | --- | --- |
| block | System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\> | The object that is being visited. |

### ReturnValue

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.
## Remarks


Note: A building block node and its children are not visited when you execute a Visitor over a [Document](../../document/). If you want to execute a Visitor over a building block, you need to execute the visitor over [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) or call [Accept()](../../../aspose.words.buildingblocks/buildingblock/accept/).

## See Also

* Enum [VisitorAction](../../visitoraction/)
* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
