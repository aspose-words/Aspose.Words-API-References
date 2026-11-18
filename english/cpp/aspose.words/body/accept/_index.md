---
title: Aspose::Words::Body::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Body::Accept method. Accepts a visitor in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/body/accept/
---
## Body::Accept method


Accepts a visitor.

```cpp
_Bool Aspose::Words::Body::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../documentvisitor/).

For more info see the Visitor design pattern.
 Calls [VisitBodyStart()](../../documentvisitor/visitbodystart/), then calls [Accept()](../../node/accept/) for all child nodes of the section and calls [VisitBodyEnd()](../../documentvisitor/visitbodyend/) at the end. 
## See Also

* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
