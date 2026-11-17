---
title: Aspose::Words::BuildingBlocks::GlossaryDocument::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::GlossaryDocument::Accept method. Accepts a visitor in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.buildingblocks/glossarydocument/accept/
---
## GlossaryDocument::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::BuildingBlocks::GlossaryDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

Calls [VisitGlossaryDocumentStart()](../../../aspose.words/documentvisitor/visitglossarydocumentstart/), then calls [Accept()](../../../aspose.words/node/accept/) for all child nodes of this node and then calls [VisitGlossaryDocumentEnd()](../../../aspose.words/documentvisitor/visitglossarydocumentend/) at the end.

Note: A glossary document node and its children are not visited when you execute a Visitor over a [Document](../../../aspose.words/document/). If you want to execute a Visitor over a glossary document, you need to call [Accept()](./).

## See Also

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
