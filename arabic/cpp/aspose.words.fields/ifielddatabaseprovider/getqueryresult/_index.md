---
title: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult method"
linktitle: "GetQueryResult"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult method. يُرجِع نتيجة الاستعلام في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider::GetQueryResult method


يرجع نتيجة الاستعلام.

```cpp
virtual System::SharedPtr<Aspose::Words::Fields::FieldDatabaseDataTable> Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult(System::String fileName, System::String connection, System::String query, System::SharedPtr<Aspose::Words::Fields::FieldDatabase> field)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | System::String | المسار الكامل واسم الملف لقاعدة البيانات المحددة في مفتاح الحقل \d. |
| connection | System::String | الاتصال بالبيانات المحددة في مفتاح الحقل \c. |
| استعلام | System::String | مجموعة أوامر SQL التي تستعلم عن قاعدة البيانات المحددة في مفتاح الحقل \s. |
| حقل | System::SharedPtr\<Aspose::Words::Fields::FieldDatabase\> | الحقل الذي يتم تحديثه. |

### ReturnValue

مثيل [FieldDatabaseDataTable](../../fielddatabasedatatable/) الذي يجب استخدامه لتحديث الحقل.

## انظر أيضًا

* Class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* Class [FieldDatabase](../../fielddatabase/)
* Interface [IFieldDatabaseProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
