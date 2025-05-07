---
title: DocumentVisitor.visitBuildingBlockStart method
linktitle: visitBuildingBlockStart method
articleTitle: visitBuildingBlockStart method
second_title: Aspose.Words for Node.js
description: "DocumentVisitor.visitBuildingBlockStart method. Called when enumeration of a building block has started."
type: docs
weight: 70
url: /nodejs-net/aspose.words/documentvisitor/visitBuildingBlockStart/
---

## visitBuildingBlockStart(block) {#buildingblock}

Called when enumeration of a building block has started.


```js
visitBuildingBlockStart(block: Aspose.Words.BuildingBlocks.BuildingBlock)
```

| Parameter | Type | Description |
| --- | --- | --- |
| block | [BuildingBlock](../../buildingblock/) | The object that is being visited. |

### Remarks

Note: A building block node and its children are not visited when you execute a
Visitor over a [Document](../../document/). If you want to execute a Visitor over a
building block, you need to execute the visitor over [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) or
call [BuildingBlock.accept()](../../buildingblock/accept/#documentvisitor).





### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### See Also

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

