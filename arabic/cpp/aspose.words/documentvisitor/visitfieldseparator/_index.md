---
title: "طريقة Aspose::Words::DocumentVisitor::VisitFieldSeparator"
linktitle: "VisitFieldSeparator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentVisitor::VisitFieldSeparator. تُستدعى عندما يتم العثور على فاصل حقل في المستند في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor::VisitFieldSeparator method


يتم استدعاؤه عندما يتم العثور على فاصل حقل في المستند.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldSeparator(System::SharedPtr<Aspose::Words::Fields::FieldSeparator> fieldSeparator)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldSeparator | System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\> | الكائن الذي يتم زيارته. |

### ReturnValue

قيمة [VisitorAction](../../visitoraction/) التي تحدد كيفية متابعة التعداد.
## ملاحظات


فاصل الحقل يفصل بين رمز الحقل وقيمة الحقل في المستند. لاحظ أن بعض الحقول تحتوي فقط على رمز الحقل ولا تحتوي على فاصل الحقل أو قيمة الحقل.

لمزيد من المعلومات راجع [VisitFieldStart()](../visitfieldstart/)

## انظر أيضًا

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
