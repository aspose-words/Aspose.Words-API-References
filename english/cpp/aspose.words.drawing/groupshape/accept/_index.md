---
title: Aspose::Words::Drawing::GroupShape::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::GroupShape::Accept method. Accepts a visitor in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.drawing/groupshape/accept/
---
## GroupShape::Accept method


Accepts a visitor.

```cpp
_Bool Aspose::Words::Drawing::GroupShape::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.
 Calls [VisitGroupShapeStart()](../../../aspose.words/documentvisitor/visitgroupshapestart/), then calls [Accept()](../../../aspose.words/node/accept/) for all child shapes of this group shape and calls [VisitGroupShapeEnd()](../../../aspose.words/documentvisitor/visitgroupshapeend/) at the end. 
## See Also

* Class [GroupShape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
