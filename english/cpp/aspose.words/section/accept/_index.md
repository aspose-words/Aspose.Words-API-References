---
title: Accept
second_title: Aspose.Words for C++ API Reference
description: Accepts a visitor.
type: docs
weight: 27
url: /cpp/aspose.words/section/accept/
---
## Section::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::Section::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
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
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
