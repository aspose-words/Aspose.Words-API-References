---
title: "طريقة Aspose::Words::EditableRange::get_SingleUser"
linktitle: "get_SingleUser"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::EditableRange::get_SingleUser. تُرجع أو تُعيّن المستخدم الفردي لنطاق التحرير في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/editablerange/get_singleuser/
---
## EditableRange::get_SingleUser method


يعيد أو يضبط المستخدم الفردي للنطاق القابل للتحرير.

```cpp
System::String Aspose::Words::EditableRange::get_SingleUser()
```

## ملاحظات


يمكن تخزين هذا المحرر بأحد الأشكال التالية:

DOMAIN\\Username - للمستخدمين الذين سيتم توثيق وصولهم باستخدام بيانات اعتماد نطاق المستخدم الحالي.

user@domain.com - للمستخدمين الذين سيتم توثيق وصولهم باستخدام عنوان البريد الإلكتروني للمستخدم كبيانات اعتماد.

user - للمستخدمين الذين سيتم توثيق وصولهم باستخدام بيانات اعتماد جهاز المستخدم الحالي.

لا يمكن تعيين المستخدم الفردي ومجموعة المحرر في نفس الوقت للنطاق القابل للتحرير المحدد؛ إذا تم تعيين أحدهما، سيُمسح الآخر.
## انظر أيضًا

* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
