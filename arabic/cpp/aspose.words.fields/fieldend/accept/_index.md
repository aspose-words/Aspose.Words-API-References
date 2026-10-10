---
title: "طريقة Aspose::Words::Fields::FieldEnd::Accept"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldEnd::Accept. تقبل زائرًا في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldend/accept/
---
## FieldEnd::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::Fields::FieldEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقدة. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## ملاحظات


ينادي [VisitFieldEnd()](../../../aspose.words/documentvisitor/visitfieldend/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

## انظر أيضًا

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldEnd](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
