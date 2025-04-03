---
title: BuildingBlock.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for NodeJs
description: "BuildingBlock.accept method. Accepts a visitor."
type: docs
weight: 130
url: /nodejs-net/Aspose.Words/buildingblock/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```js
accept(visitor: Aspose.Words.DocumentVisitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../documentvisitor/) | The visitor that will visit the nodes. |

### Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visitBuildingBlockStart()](../../documentvisitor/visitBuildingBlockStart/#buildingblock), then calls 
[Node.accept()](../../node/accept/#documentvisitor) for all child nodes of this building block, then calls 
[DocumentVisitor.visitBuildingBlockEnd()](../../documentvisitor/visitBuildingBlockEnd/#buildingblock).




Note: A building block node and its children are not visited when you execute a
Visitor over a [Document](../../document/). If you want to execute a Visitor over a
building block, you need to execute the visitor over [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) or
call [BuildingBlock.accept()](./#documentvisitor).





### Returns

True if all nodes were visited; false if [DocumentVisitor](../../documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [Aspose.Words](../../)
* class [BuildingBlock](../)

