---
title: "طريقة Aspose::Words::Run::Accept"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Run::Accept. تقبل زائرًا في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/run/accept/
---
## Run::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::Run::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقدة. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## ملاحظات


ينادي [VisitRun()](../../documentvisitor/visitrun/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

## انظر أيضًا

* Class [DocumentVisitor](../../documentvisitor/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
