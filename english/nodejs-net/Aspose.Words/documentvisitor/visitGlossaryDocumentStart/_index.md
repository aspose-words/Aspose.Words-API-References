---
title: DocumentVisitor.visitGlossaryDocumentStart method
linktitle: visitGlossaryDocumentStart method
articleTitle: visitGlossaryDocumentStart method
second_title: Aspose.Words for NodeJs
description: "DocumentVisitor.visitGlossaryDocumentStart method. Called when enumeration of a glossary document has started."
type: docs
weight: 250
url: /nodejs-net/aspose.words/documentvisitor/visitGlossaryDocumentStart/
---

## visitGlossaryDocumentStart(glossary) {#glossarydocument}

Called when enumeration of a glossary document has started.


```js
visitGlossaryDocumentStart(glossary: Aspose.Words.BuildingBlocks.GlossaryDocument)
```

| Parameter | Type | Description |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) | The object that is being visited. |

### Remarks

Note: A glossary document node and its children are not visited when you execute a
Visitor over a [Document](../../document/). If you want to execute a Visitor over a
glossary document, you need to call [GlossaryDocument.accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/#documentvisitor).





### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### See Also

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

