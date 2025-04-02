---
title: Shape.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for NodeJs
description: "Shape.accept method. Accepts a visitor."
type: docs
weight: 250
url: /nodejs-net/Aspose.Words.Drawing/shape/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```js
accept(visitor: Aspose.Words.DocumentVisitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../../Aspose.Words/documentvisitor/) | The visitor that will visit the nodes. |

### Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../Aspose.Words/documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visitShapeStart()](../../../Aspose.Words/documentvisitor/visitShapeStart/#shape), then calls [Node.accept()](../../../Aspose.Words/node/accept/#documentvisitor)
for all child nodes of the shape and calls [DocumentVisitor.visitShapeEnd()](../../../Aspose.Words/documentvisitor/visitShapeEnd/#shape) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../Aspose.Words/documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [Aspose.Words.Drawing](../../)
* class [Shape](../)

