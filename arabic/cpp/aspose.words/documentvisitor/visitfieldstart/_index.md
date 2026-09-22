---
title: "Aspose::Words::DocumentVisitor::VisitFieldStart طريقة"
linktitle: "VisitFieldStart"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentVisitor::VisitFieldStart طريقة. تُستدعى عندما يبدأ حقل في المستند في C++."
type: docs
weight: 23000
url: /ar/cpp/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor::VisitFieldStart method


يتم استدعاؤه عندما يبدأ حقل في المستند.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldStart(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldStart | System::SharedPtr\<Aspose::Words::Fields::FieldStart\> | الكائن الذي يتم زيارته. |

### ReturnValue

قيمة [VisitorAction](../../visitoraction/) التي تحدد كيفية متابعة التعداد.
## ملاحظات


يتكون الحقل في مستند Word من رمز الحقل وقيمة الحقل.

على سبيل المثال، يمكن تمثيل حقل يعرض رقم الصفحة كما يلي:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

فاصل الحقل يفصل بين رمز الحقل وقيمة الحقل في المستند. لاحظ أن بعض الحقول تحتوي فقط على رمز الحقل ولا تحتوي على فاصل الحقل أو قيمة الحقل.

[Fields](../../../aspose.words.fields/) can be nested.

## انظر أيضًا

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldStart](../../../aspose.words.fields/fieldstart/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
