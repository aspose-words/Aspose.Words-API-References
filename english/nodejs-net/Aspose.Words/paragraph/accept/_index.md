﻿---
title: Paragraph.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Node.js
description: "Paragraph.accept method. Accepts a visitor."
type: docs
weight: 230
url: /nodejs-net/aspose.words/paragraph/accept/
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




Calls [DocumentVisitor.visitParagraphStart()](../../documentvisitor/visitParagraphStart/#paragraph), then calls [Node.accept()](../../node/accept/#documentvisitor) for all child nodes
of the paragraph and calls [DocumentVisitor.visitParagraphEnd()](../../documentvisitor/visitParagraphEnd/#paragraph) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

