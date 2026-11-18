---
title: Aspose::Words::Tables::Cell::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Cell::Accept method. Accepts a visitor in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.tables/cell/accept/
---
## Cell::Accept method


Accepts a visitor.

```cpp
_Bool Aspose::Words::Tables::Cell::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.
 Calls [VisitCellStart()](../../../aspose.words/documentvisitor/visitcellstart/), then calls [Accept()](../../../aspose.words/node/accept/) for all child nodes of the section and calls [VisitCellEnd()](../../../aspose.words/documentvisitor/visitcellend/) at the end. 
## See Also

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
