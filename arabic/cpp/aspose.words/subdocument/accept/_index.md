---
title: "طريقة Aspose::Words::SubDocument::Accept"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::SubDocument::Accept. تقبل زائرًا في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/subdocument/accept/
---
## SubDocument::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::SubDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقد. |

### ReturnValue

صحيح إذا تم زيارة جميع العقد؛ خطأ إذا أوقف [DocumentVisitor](../../documentvisitor/) العملية قبل زيارة جميع العقد.
## ملاحظات


يُعدد هذا العقد وجميع أبنائه. كل عقدة تستدعي الطريقة المقابلة على [DocumentVisitor](../../documentvisitor/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

## انظر أيضًا

* Class [DocumentVisitor](../../documentvisitor/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
