---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeEnd::Accept طريقة"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeEnd::Accept طريقة. تقبل زائرًا في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.markup/structureddocumenttagrangeend/accept/
---
## StructuredDocumentTagRangeEnd::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTagRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقد. |

### ReturnValue

صحيح إذا تم زيارة جميع العقد؛ خطأ إذا أوقف [DocumentVisitor](../../../aspose.words/documentvisitor/) العملية قبل زيارة جميع العقد.
## ملاحظات


يعدّ هذا العقد وجميع أبنائه. كل عقدة تستدعي الطريقة المقابلة على [DocumentVisitor](../../../aspose.words/documentvisitor/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

## انظر أيضًا

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [StructuredDocumentTagRangeEnd](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
