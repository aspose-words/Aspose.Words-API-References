---
title: GroupShape.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for NodeJs
description: "GroupShape.accept method. Accepts a visitor."
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing/groupshape/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```js
accept(visitor: Aspose.Words.DocumentVisitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../../aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

### Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visitGroupShapeStart()](../../../aspose.words/documentvisitor/visitGroupShapeStart/#groupshape), then calls [Node.accept()](../../../aspose.words/node/accept/#documentvisitor) for all 
child shapes of this group shape and calls [DocumentVisitor.visitGroupShapeEnd()](../../../aspose.words/documentvisitor/visitGroupShapeEnd/#groupshape) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [Aspose.Words.Drawing](../../)
* class [GroupShape](../)

