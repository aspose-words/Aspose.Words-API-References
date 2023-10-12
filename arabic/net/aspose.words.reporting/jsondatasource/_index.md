---
title: Class JsonDataSource
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Reporting.JsonDataSource فصل. يوفر الوصول إلى بيانات ملف JSON أو التدفق لاستخدامه في التقرير.
type: docs
weight: 4690
url: /ar/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

يوفر الوصول إلى بيانات ملف JSON أو التدفق لاستخدامه في التقرير.

لمعرفة المزيد، قم بزيارة[محرك التقارير LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) مقالة توثيقية.

```csharp
public class JsonDataSource
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(Stream) | إنشاء مصدر بيانات جديد ببيانات من تدفق JSON باستخدام الخيارات الافتراضية لتحليل بيانات JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(string) | إنشاء مصدر بيانات جديد ببيانات من ملف JSON باستخدام الخيارات الافتراضية لتحليل بيانات JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(Stream, JsonDataLoadOptions) | إنشاء مصدر بيانات جديد ببيانات من تدفق JSON باستخدام الخيارات المحددة لتحليل بيانات JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(string, JsonDataLoadOptions) | إنشاء مصدر بيانات جديد ببيانات من ملف JSON باستخدام الخيارات المحددة لتحليل بيانات JSON. |

### ملاحظات

للوصول إلى بيانات الملف أو الدفق المقابل أثناء إنشاء تقرير، قم بتمرير مثيل من هذه الفئة as مصدر بيانات إلى أحدها[`ReportingEngine`](../reportingengine/) .BuildReport الحمولة الزائدة.

في مستندات القالب، إذا كان عنصر JSON ذو المستوى الأعلى عبارة عن مصفوفة، فسيتم استخدام أ`JsonDataSource` يجب أن يتم التعامل مع المثيل بنفس الطريقة كما لو كانDataTable مثيل. إذا كان عنصر JSON ذو المستوى الأعلى عبارة عن كائن، أ`JsonDataSource` يجب التعامل مع المثيل بنفس الطريقة كما لو كان aDataRow مثيل. لمزيد من المعلومات، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

في مستندات القالب، يمكنك العمل مع القيم المكتوبة لعناصر JSON. للراحة، يستبدل المحرك المجموعة من أنواع JSON البسيطة بالنوع التالي:

* Nullable
* Nullable
* Nullable
* Nullable
* String

يتعرف المحرك تلقائيًا على قيم الأنواع الإضافية بناءً على تمثيلات JSON الخاصة بها.

لتجاوز السلوك الافتراضي لتحميل بيانات JSON، قم بتهيئة وتمرير ملف[`JsonDataLoadOptions`](../jsondataloadoptions/) example إلى منشئ هذه الفئة.

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)


