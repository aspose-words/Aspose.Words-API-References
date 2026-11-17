---
title: Aspose::Words::Node::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Node::Accept method. Accepts a visitor in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/node/accept/
---
## Node::Accept method


Accepts a visitor.

```cpp
virtual bool Aspose::Words::Node::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../documentvisitor/).

For more info see the Visitor design pattern.

## See Also

* Class [DocumentVisitor](../../documentvisitor/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
