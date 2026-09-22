---
title: "Aspose::Words::Settings::OdsoDataSourceType enum"
linktitle: "OdsoDataSourceType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::OdsoDataSourceType enum. يحدد نوع مصدر البيانات الخارجي الذي سيتم الاتصال به كجزء من معلومات اتصال ODSO في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enum


يحدد نوع مصدر البيانات الخارجي الذي سيتم الاتصال به كجزء من معلومات اتصال ODSO.

```cpp
enum class OdsoDataSourceType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Text | 0 | يحدد أن المستند المعطى قد تم ربطه بملف نصي. ربما wdMergeSubTypeOther. |
| Database | 1 | يحدد أن المستند المعطى قد تم ربطه بقاعدة بيانات. ربما wdMergeSubTypeAccess. |
| دفتر العناوين | 2 | يحدد أن المستند المحدد قد تم ربطه بدفتر عناوين جهات الاتصال. ربما wdMergeSubTypeOAL. |
| Document1 | 3 | يحدد أن المستند المحدد قد تم ربطه بتنسيق مستند آخر يدعمه التطبيق المنتج. ربما wdMergeSubTypeOLEDBWord. |
| Document2 | 4 | يحدد أن المستند المحدد قد تم ربطه بتنسيق مستند آخر يدعمه التطبيق المنتج. ربما wdMergeSubTypeWorks. |
| Native | 5 | يحدد أن المستند المحدد قد تم ربطه بتنسيق مستند أصلي للتطبيق المنتج. ربما wdMergeSubTypeOLEDBText. |
| Email | 6 | يحدد أن المستند المحدد قد تم ربطه بتطبيق بريد إلكتروني. ربما wdMergeSubTypeOutlook. |
| None | 7 | نوع مصدر البيانات الخارجي غير محدد. ربما wdMergeSubTypeWord. |
| تقليدي | 8 | يحدد أن المستند المحدد قد تم ربطه بتنسيق مستند تقليدي يدعمه التطبيق المنتج ربما wdMergeSubTypeWord2000. |
| رئيسي | 9 | يحدد أن المستند المحدد قد تم ربطه بمصدر بيانات يجمع مصادر بيانات أخرى. |
| Default | n/a | يساوي [None](./). |

## ملاحظات


مواصفة OOXML غير واضحة جدًا لهذا التعداد. أعتقد أنه قد يتطابق مع تعداد WdMergeSubType [http://msdn.microsoft.com/en-us/library/bb237801.aspx](http://msdn.microsoft.com/en-us/library/bb237801.aspx).

## انظر أيضًا

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
