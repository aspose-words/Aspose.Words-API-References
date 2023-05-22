---
title: BuildingBlock.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "BuildingBlock.accept method. Accepts a visitor."
type: docs
weight: 130
url: /python-net/aspose.words.buildingblocks/buildingblock/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```python
def accept(self, visitor: aspose.words.DocumentVisitor):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../../aspose.words/documentvisitor/) |  |

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visit_building_block_start()](../../../aspose.words/documentvisitor/visit_building_block_start/#buildingblock), then calls 
[Node.accept()](../../../aspose.words/node/accept/#documentvisitor) for all child nodes of this building block, then calls 
[DocumentVisitor.visit_building_block_end()](../../../aspose.words/documentvisitor/visit_building_block_end/#buildingblock).




Note: A building block node and its children are not visited when you execute a
Visitor over a [Document](../../../aspose.words/document/). If you want to execute a Visitor over a
building block, you need to execute the visitor over [GlossaryDocument](../../glossarydocument/) or
call [BuildingBlock.accept()](./#documentvisitor).





### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [aspose.words.buildingblocks](../../)
* class [BuildingBlock](../)

