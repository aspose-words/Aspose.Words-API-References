---
title: "طريقة Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion"
linktitle: "GetFieldNamesForRegion"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion. تُرجع مجموعة من أسماء حقول دمج البريد المتاحة في المنطقة في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## MailMerge::GetFieldNamesForRegion(const System::String\&) method


يرجع مجموعة من أسماء حقول دمج البريد المتوفرة في المنطقة.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| regionName | const System::String\& | اسم المنطقة (غير حساس لحالة الأحرف). |
## ملاحظات


يرجع أسماء حقول الدمج الكاملة بما في ذلك البادئة الاختيارية. لا يزيل أسماء الحقول المكررة.

إذا كان المستند يحتوي على عدة مناطق بنفس الاسم، يتم معالجة أول منطقة فقط.

يتم إنشاء مصفوفة سلاسل جديدة في كل استدعاء.

## انظر أيضًا

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::GetFieldNamesForRegion(const System::String\&, int32_t) method


يرجع مجموعة من أسماء حقول دمج البريد المتوفرة في المنطقة.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName, int32_t regionIndex)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| regionName | const System::String\& | اسم المنطقة (غير حساس لحالة الأحرف). |
| regionIndex | int32_t | فهرس المنطقة (مبني على الصفر). |
## ملاحظات


يرجع أسماء حقول الدمج الكاملة بما في ذلك البادئة الاختيارية. لا يزيل أسماء الحقول المكررة.

إذا كان المستند يحتوي على عدة مناطق بنفس الاسم، يتم معالجة المنطقة رقم N (مبني على الصفر).

يتم إنشاء مصفوفة سلاسل جديدة في كل استدعاء.

## انظر أيضًا

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
