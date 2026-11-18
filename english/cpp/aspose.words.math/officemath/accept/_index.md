---
title: Aspose::Words::Math::OfficeMath::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Math::OfficeMath::Accept method. Accepts a visitor in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.math/officemath/accept/
---
## OfficeMath::Accept method


Accepts a visitor.

```cpp
_Bool Aspose::Words::Math::OfficeMath::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.
 Calls [VisitOfficeMathStart()](../../../aspose.words/documentvisitor/visitofficemathstart/), then calls [Accept()](../../../aspose.words/node/accept/) for all child nodes of the Office Math and calls [VisitOfficeMathEnd()](../../../aspose.words/documentvisitor/visitofficemathend/) at the end. 
## See Also

* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
