---
title: "Aspose::Words::Body::Accept طريقة"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Body::Accept طريقة. يقبل زائرًا في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/body/accept/
---
## Body::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::Body::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
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
* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
