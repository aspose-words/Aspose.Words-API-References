---
title: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource طريقة"
linktitle: "GetDataSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource طريقة. يستدعي محرك دمج البريد Aspose.Words هذه الطريقة عندما يصادف بداية منطقة دمج بريد من المستوى الأعلى في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


محرك دمج البريد Aspose.Words يستدعي هذه الطريقة عندما يصادف بداية منطقة دمج بريد من المستوى الأعلى.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| tableName | System::String | اسم منطقة دمج البريد كما هو محدد في مستند القالب. غير حساس لحالة الأحرف. |

### ReturnValue

كائن مصدر بيانات سيوفر الوصول إلى سجلات البيانات للجدول المحدد.
## ملاحظات


عندما يقوم محرك دمج البريد Aspose.Words بملء مستند بالبيانات ويصادف MERGEFIELD TableStart:TableName، فإنه يستدعي [GetDataSource()](./) على هذا الكائن. يحتاج تنفيذك إلى إرجاع كائن مصدر بيانات جديد. سيستخدم Aspose.Words مصدر البيانات المُرجع لملء منطقة دمج البريد.

إذا لم يكن هناك مصدر بيانات (جدول) بالاسم المحدد، يجب على تنفيذك إرجاع **null**.

## انظر أيضًا

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
