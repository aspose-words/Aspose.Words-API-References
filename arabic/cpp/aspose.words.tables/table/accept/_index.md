---
title: "Aspose::Words::Tables::Table::Accept طريقة"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::Accept طريقة. يقبل زائرًا في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.tables/table/accept/
---
## Table::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::Tables::Table::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
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
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
