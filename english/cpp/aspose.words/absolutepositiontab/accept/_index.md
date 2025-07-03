---
title: Aspose::Words::AbsolutePositionTab::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AbsolutePositionTab::Accept method. Accepts a visitor in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::AbsolutePositionTab::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the node. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Remarks


Calls [VisitAbsolutePositionTab()](../../documentvisitor/visitabsolutepositiontab/).

For more info see the Visitor design pattern.

## See Also

* Class [DocumentVisitor](../../documentvisitor/)
* Class [AbsolutePositionTab](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
