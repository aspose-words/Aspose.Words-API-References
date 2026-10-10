---
title: "طريقة Aspose::Words::AbsolutePositionTab::Accept"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::AbsolutePositionTab::Accept. تقبل زائرًا في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::AbsolutePositionTab::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقدة. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## ملاحظات


ينادي [VisitAbsolutePositionTab()](../../documentvisitor/visitabsolutepositiontab/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

## انظر أيضًا

* Class [DocumentVisitor](../../documentvisitor/)
* Class [AbsolutePositionTab](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
