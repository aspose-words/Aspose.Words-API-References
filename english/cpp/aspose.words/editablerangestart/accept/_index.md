---
title: Aspose::Words::EditableRangeStart::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EditableRangeStart::Accept method. Accepts a visitor in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/editablerangestart/accept/
---
## EditableRangeStart::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::EditableRangeStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the node. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Remarks


Calls [VisitEditableRangeStart()](../../documentvisitor/visiteditablerangestart/).

For more info see the Visitor design pattern.

## See Also

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
