---
title: GlossaryDocument.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for NodeJs
description: "GlossaryDocument.accept method. Accepts a visitor."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.BuildingBlocks/glossarydocument/accept/
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




Calls [DocumentVisitor.visitGlossaryDocumentStart()](../../../aspose.words/documentvisitor/visitGlossaryDocumentStart/#glossarydocument), then calls [Node.accept()](../../../aspose.words/node/accept/#documentvisitor)
for all child nodes of this node and then calls [DocumentVisitor.visitGlossaryDocumentEnd()](../../../aspose.words/documentvisitor/visitGlossaryDocumentEnd/#glossarydocument)
at the end.




Note: A glossary document node and its children are not visited when you execute a
Visitor over a [Document](../../../aspose.words/document/). If you want to execute a Visitor over a
glossary document, you need to call [GlossaryDocument.accept()](./#documentvisitor).





### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### See Also

* module [Aspose.Words.BuildingBlocks](../../)
* class [GlossaryDocument](../)

