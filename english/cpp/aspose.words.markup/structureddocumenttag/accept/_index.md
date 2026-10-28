---
title: Aspose::Words::Markup::StructuredDocumentTag::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::Accept method. Accepts a visitor in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.markup/structureddocumenttag/accept/
---
## StructuredDocumentTag::Accept method


Accepts a visitor.

```cpp
_Bool Aspose::Words::Markup::StructuredDocumentTag::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.
 Calls [VisitStructuredDocumentTagStart()](../../../aspose.words/documentvisitor/visitstructureddocumenttagstart/), then calls [Accept()](../../../aspose.words/node/accept/) for all child nodes of the smart tag and calls [VisitStructuredDocumentTagEnd()](../../../aspose.words/documentvisitor/visitstructureddocumenttagend/) at the end. 
## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
