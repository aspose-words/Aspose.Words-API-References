---
title: "طريقة Aspose::Words::Node::Accept"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Node::Accept. تقبل زائرًا في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/node/accept/
---
## Node::Accept method


يقبل زائرًا.

```cpp
virtual bool Aspose::Words::Node::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor)=0
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
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
