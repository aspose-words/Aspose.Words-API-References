---
title: "طريقة Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions"
linktitle: "ExecuteWithRegions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions. تقوم بإجراء دمج بريد من مصدر بيانات مخصص مع مناطق دمج البريد في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


ينفّذ دمج بريد من مصدر بيانات مخصص مع مناطق دمج البريد.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | كائن ينفّذ واجهة مصدر بيانات دمج البريد المخصصة. |
## ملاحظات


استخدم هذه الطريقة لملء حقول دمج البريد في المستند بالقيم من أي مصدر بيانات مخصص مثل ملف XML أو مجموعات من كائنات الأعمال. تحتاج إلى كتابة فئتك الخاصة التي تنفّذ واجهة [IMailMergeDataSource](../../imailmergedatasource/) .

يمكنك استخدام هذه الطريقة فقط عندما تكون [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) **false**، أي أنك لا تحتاج إلى توافق مع اللغات من اليمين إلى اليسار (مثل العربية أو العبرية).

## انظر أيضًا

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) method


ينفّذ دمج بريد من مصدر بيانات مخصص مع مناطق دمج البريد.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSourceRoot> &dataSourceRoot)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| dataSourceRoot | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\& | كائن ينفّذ واجهة مصدر بيانات دمج البريد المخصص الجذر. |
## ملاحظات


استخدم هذه الطريقة لملء حقول دمج البريد في المستند بالقيم من أي مصدر بيانات مخصص مثل ملف XML أو مجموعات من كائنات الأعمال. تحتاج إلى كتابة فئاتك الخاصة التي تنفّذ واجهتي [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) و [IMailMergeDataSource](../../imailmergedatasource/) .

يمكنك استخدام هذه الطريقة فقط عندما تكون [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) **false**، أي أنك لا تحتاج إلى توافق مع اللغات من اليمين إلى اليسار (مثل العربية أو العبرية).

## انظر أيضًا

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
