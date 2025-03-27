---
title: DocumentVisitor.visitBuildingBlockEnd method
linktitle: visitBuildingBlockEnd method
articleTitle: visitBuildingBlockEnd method
second_title: Aspose.Words for NodeJs
description: "DocumentVisitor.visitBuildingBlockEnd method. Called when enumeration of a building block has ended."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words/documentvisitor/visitBuildingBlockEnd/
---

## visitBuildingBlockEnd(block) {#buildingblock}

Called when enumeration of a building block has ended.


```js
visitBuildingBlockEnd(block: Aspose.Words.BuildingBlocks.BuildingBlock)
```

| Parameter | Type | Description |
| --- | --- | --- |
| block | [BuildingBlock](../../buildingblock/) | The object that is being visited. |

### Remarks

Note: A building block node and its children are not visited when you execute a
Visitor over a [Document](../../document/). If you want to execute a Visitor over a
building block, you need to execute the visitor over [GlossaryDocument](../../../Aspose.Words.BuildingBlocks/glossarydocument/) or
call [BuildingBlock.accept()](../../buildingblock/accept/#documentvisitor).





### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### See Also

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

