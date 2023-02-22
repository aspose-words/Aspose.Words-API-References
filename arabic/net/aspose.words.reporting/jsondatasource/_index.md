---
title: Class JsonDataSource
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Reporting.JsonDataSource فصل. يوفر الوصول إلى بيانات ملف JSON أو دفق لاستخدامه في تقرير .
type: docs
weight: 4430
url: /ar/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

يوفر الوصول إلى بيانات ملف JSON أو دفق لاستخدامه في تقرير .

```csharp
public class JsonDataSource
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(Stream) | إنشاء مصدر بيانات جديد ببيانات من دفق JSON باستخدام الخيارات الافتراضية لتحليل بيانات JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(string) | إنشاء مصدر بيانات جديد ببيانات من ملف JSON باستخدام الخيارات الافتراضية لتحليل بيانات JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(Stream, JsonDataLoadOptions) | إنشاء مصدر بيانات جديد ببيانات من دفق JSON باستخدام الخيارات المحددة لتحليل بيانات JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(string, JsonDataLoadOptions) | إنشاء مصدر بيانات جديد ببيانات من ملف JSON باستخدام الخيارات المحددة لتحليل بيانات JSON. |

### ملاحظات

للوصول إلى بيانات الملف أو الدفق المقابل أثناء إنشاء تقرير ، قم بتمرير مثيل من هذه الفئة كـ مصدر بيانات إلى أحد[`ReportingEngine`](../reportingengine/) إنشاء تقرير عن الحمولة الزائدة.

في مستندات النموذج ، إذا كان عنصر JSON ذو المستوى الأعلى عبارة عن مصفوفة ، أ`JsonDataSource` يجب معاملة المثال be بنفس الطريقة كما لو كان ملفDataTable مثيل. إذا كان عنصر JSON عالي المستوى كائنًا ، فإن ملف`JsonDataSource` يجب معاملة المثيل بنفس الطريقة كما لو كان أDataRow مثيل. لمزيد من المعلومات ، راجع مرجع بناء الجملة (https://docs.aspose.com/display/wordsnet/Template+Syntax).

في مستندات النموذج ، يمكنك التعامل مع القيم المكتوبة لعناصر JSON. للراحة ، يستبدل المحرك مجموعة لأنواع JSON البسيطة بالمجموعة التالية:

* Nullable
* Nullable
* Nullable
* Nullable
* String

يتعرف المحرك تلقائيًا على قيم الأنواع الإضافية بناءً على تمثيلات JSON الخاصة بهم.

لتجاوز السلوك الافتراضي لتحميل بيانات JSON ، قم بتهيئة وتمرير ملف[`JsonDataLoadOptions`](../jsondataloadoptions/)example إلى مُنشئ هذه الفئة.

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)


