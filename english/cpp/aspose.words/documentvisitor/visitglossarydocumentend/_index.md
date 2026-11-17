---
title: Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd method
linktitle: VisitGlossaryDocumentEnd
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd method. Called when enumeration of a glossary document has ended in C++.'
type: docs
weight: 27000
url: /cpp/aspose.words/documentvisitor/visitglossarydocumentend/
---
## DocumentVisitor::VisitGlossaryDocumentEnd method


Called when enumeration of a glossary document has ended.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
```


| Parameter | Type | Description |
| --- | --- | --- |
| glossary | System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> | The object that is being visited. |

### ReturnValue

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.
## Remarks


Note: A glossary document node and its children are not visited when you execute a Visitor over a [Document](../../document/). If you want to execute a Visitor over a glossary document, you need to call [Accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/).

## See Also

* Enum [VisitorAction](../../visitoraction/)
* Class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
