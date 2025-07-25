---
title: Aspose::Words::EditableRangeEnd::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EditableRangeEnd::Accept method. Accepts a visitor in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/editablerangeend/accept/
---
## EditableRangeEnd::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::EditableRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the node. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Remarks


Calls [VisitEditableRangeEnd()](../../documentvisitor/visiteditablerangeend/).

For more info see the Visitor design pattern.

## See Also

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
