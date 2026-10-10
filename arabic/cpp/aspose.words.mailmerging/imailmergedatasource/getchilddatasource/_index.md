---
title: "طريقة Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource"
linktitle: "GetChildDataSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource. يستدعي محرك دمج البريد Aspose.Words هذه الطريقة عندما يصادف بداية منطقة دمج بريد متداخلة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource::GetChildDataSource method


محرك دمج البريد Aspose.Words يستدعي هذه الطريقة عندما يصادف بداية منطقة دمج بريد متداخلة.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource(System::String tableName)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| tableName | System::String | اسم منطقة دمج البريد كما هو محدد في مستند القالب. غير حساس لحالة الأحرف. |

### ReturnValue

كائن مصدر بيانات سيوفر الوصول إلى سجلات البيانات للجدول المحدد.
## ملاحظات


عند قيام محركات دمج البريد Aspose.Words بملء منطقة دمج البريد بالبيانات وصادفت بداية منطقة دمج بريد متداخلة على شكل MERGEFIELD TableStart:TableName، تستدعي [GetChildDataSource()](./) على كائن مصدر البيانات الحالي. يحتاج تنفيذك إلى إرجاع كائن مصدر بيانات جديد سيوفر الوصول إلى سجلات الطفل للسجل الأب الحالي. سيستخدم Aspose.Words مصدر البيانات المرجع لملء منطقة دمج البريد المتداخلة.

فيما يلي القواعد التي يجب أن يتبعها تنفيذ [GetChildDataSource()](./).

إذا كان الجدول الممثل بهذا الكائن مصدر البيانات يحتوي على جدول فرعي (تفصيلي) مرتبط بالاسم المحدد، يجب على تنفيذك إرجاع كائن [IMailMergeDataSource](../) جديد سيوفر الوصول إلى سجلات الطفل للسجل الحالي. مثال على ذلك علاقة Orders / OrderDetails. لنفترض أن كائن [IMailMergeDataSource](../) الحالي يمثل جدول Orders ولديه سجل طلب حالي. بعد ذلك، يصادف Aspose.Words \"MERGEFIELD TableStart:OrderDetails\" في المستند ويستدعي [GetChildDataSource()](./). تحتاج إلى إنشاء وإرجاع كائن [IMailMergeDataSource](../) يسمح لـ Aspose.Words بالوصول إلى سجل OrderDetails للطلب الحالي.

إذا لم يكن لهذا الكائن مصدر البيانات علاقة بالجدول بالاسم المحدد، فأنت بحاجة إلى إرجاع كائن [IMailMergeDataSource](../) سيوفر الوصول إلى جميع سجلات الجدول المحدد.

إذا لم يكن هناك جدول بالاسم المحدد، يجب على تنفيذك إرجاع **null**.

## انظر أيضًا

* Interface [IMailMergeDataSource](../)
* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
