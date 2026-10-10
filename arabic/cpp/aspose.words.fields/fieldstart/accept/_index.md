---
title: "طريقة Accept في Aspose::Words::Fields::FieldStart"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Accept في Aspose::Words::Fields::FieldStart. تقبل زائرًا في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldstart/accept/
---
## FieldStart::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::Fields::FieldStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقدة. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## ملاحظات


تستدعي [VisitFieldStart()](../../../aspose.words/documentvisitor/visitfieldstart/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

## انظر أيضًا

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
