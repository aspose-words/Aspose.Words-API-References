---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Reporting.CsvDataSource فصل. يوفر الوصول إلى بيانات ملف CSV أو الدفق لاستخدامها في التقرير في C#.
type: docs
weight: 4670
url: /ar/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

يوفر الوصول إلى بيانات ملف CSV أو الدفق لاستخدامها في التقرير.

لمعرفة المزيد، قم بزيارة[محرك التقارير LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) مقالة توثيقية.

```csharp
public class CsvDataSource
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | إنشاء مصدر بيانات جديد ببيانات من تدفق CSV باستخدام الخيارات الافتراضية لتحليل بيانات CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | إنشاء مصدر بيانات جديد ببيانات من ملف CSV باستخدام الخيارات الافتراضية لتحليل بيانات CSV. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | إنشاء مصدر بيانات جديد ببيانات من تدفق CSV باستخدام الخيارات المحددة لتحليل بيانات CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | إنشاء مصدر بيانات جديد ببيانات من ملف CSV باستخدام الخيارات المحددة لتحليل بيانات CSV. |

## ملاحظات

للوصول إلى بيانات الملف أو الدفق المقابل أثناء إنشاء تقرير، قم بتمرير مثيل من هذه الفئة as مصدر بيانات إلى أحدها[`ReportingEngine`](../reportingengine/) .BuildReport الحمولة الزائدة.

في مستندات القالب، أ`CsvDataSource` يجب التعامل مع المثيل بنفس الطريقة كما لو كان aDataTable مثيل. لمزيد من المعلومات، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

يتم تحديد أنواع البيانات ذات القيم المفصولة بفواصل تلقائيًا بناءً على تمثيلات السلسلة الخاصة بها. لذا، في مستندات template ، يمكنك العمل باستخدام القيم المكتوبة بدلاً من السلاسل فقط. المحرك قادر على التعرف تلقائيًا على قيم من الأنواع التالية:

* Nullable
* Nullable
* Nullable
* Nullable
* String

لاحظ أنه لكي يعمل التعرف التلقائي على أنواع البيانات، يجب تشكيل تمثيلات سلسلة للقيم المفصولة بفواصل باستخدام إعدادات الثقافة الثابتة.

لتجاوز السلوك الافتراضي لتحميل بيانات CSV، قم بتهيئة وتمرير ملف[`CsvDataLoadOptions`](../csvdataloadoptions/) example إلى منشئ هذه الفئة.

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)
