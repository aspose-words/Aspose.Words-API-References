---
title: Accept
second_title: Aspose.Words for C++ API Reference
description: Accepts a visitor.
type: docs
weight: 1
url: /cpp/aspose.words/specialchar/accept/
---
## SpecialChar.Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::SpecialChar::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the node. |

### ReturnValue


False if the visitor requested the enumeration to stop.

Calls [DocumentVisitor.VisitSpecialChar](../../documentvisitor/visitspecialchar/).

For more info see the Visitor design pattern.


