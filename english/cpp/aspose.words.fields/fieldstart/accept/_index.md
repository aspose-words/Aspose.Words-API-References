---
title: Aspose::Words::Fields::FieldStart::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldStart::Accept method. Accepts a visitor in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldstart/accept/
---
## FieldStart::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::Fields::FieldStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the node. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Remarks


Calls [VisitFieldStart()](../../../aspose.words/documentvisitor/visitfieldstart/).

For more info see the Visitor design pattern.

## See Also

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
