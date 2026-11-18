---
title: Aspose::Words::Comment::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comment::Accept method. Accepts a visitor in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/comment/accept/
---
## Comment::Accept method


Accepts a visitor.

```cpp
_Bool Aspose::Words::Comment::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../documentvisitor/).

For more info see the Visitor design pattern.
 Calls [VisitCommentStart()](../../documentvisitor/visitcommentstart/), then calls [Accept()](../../node/accept/) for all child nodes of the comment and calls [VisitCommentEnd()](../../documentvisitor/visitcommentend/) at the end. 
## See Also

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
