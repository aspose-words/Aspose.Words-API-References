﻿---
title: DocumentVisitor.visitGlossaryDocumentEnd method
linktitle: visitGlossaryDocumentEnd method
articleTitle: visitGlossaryDocumentEnd method
second_title: Aspose.Words for Node.js
description: "DocumentVisitor.visitGlossaryDocumentEnd method. Called when enumeration of a glossary document has ended."
type: docs
weight: 240
url: /nodejs-net/aspose.words/documentvisitor/visitGlossaryDocumentEnd/
---

## visitGlossaryDocumentEnd(glossary) {#glossarydocument}

Called when enumeration of a glossary document has ended.


```js
visitGlossaryDocumentEnd(glossary: Aspose.Words.BuildingBlocks.GlossaryDocument)
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

