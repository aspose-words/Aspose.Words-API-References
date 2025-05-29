---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words لـ .NET
description: طوّر تقاريرك باستخدام Aspose.Words.Reporting.JsonDataSource. تمكّن من الوصول بسهولة إلى بيانات JSON لدمجها بسلاسة في تقاريرك.
type: docs
weight: 5430
url: /ar/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

يوفر الوصول إلى بيانات ملف JSON أو مجرى البيانات المراد استخدامه ضمن تقرير.

لمعرفة المزيد، قم بزيارة[محرك إعداد التقارير LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) مقالة توثيقية.

```csharp
public class JsonDataSource
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | ينشئ مصدر بيانات جديد بالبيانات من مجرى JSON باستخدام الخيارات الافتراضية لتحليل بيانات JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | ينشئ مصدر بيانات جديد بالبيانات من ملف JSON باستخدام الخيارات الافتراضية لتحليل بيانات JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | ينشئ مصدر بيانات جديد بالبيانات من مجرى JSON باستخدام الخيارات المحددة لتحليل بيانات JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | ينشئ مصدر بيانات جديد بالبيانات من ملف JSON باستخدام الخيارات المحددة لتحليل بيانات JSON. |

## ملاحظات

للوصول إلى بيانات الملف أو التدفق المقابل أثناء إنشاء تقرير، مرر مثيلًا لهذه الفئة as مصدر بيانات إلى أحد[`ReportingEngine`](../reportingengine/) .BuildReport overloads.

في مستندات القالب، إذا كان عنصر JSON من المستوى الأعلى عبارة عن مصفوفة،`JsonDataSource` يجب أن تتم معاملة المثيل بنفس الطريقة كما لو كانDataTableمثال . إذا كان عنصر JSON من المستوى الأعلى كائنًا،`JsonDataSource` يجب التعامل مع المثيل بنفس الطريقة كما لو كان aDataRow مثال . لمزيد من المعلومات، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

في مستندات القالب، يمكنك العمل مع القيم المكتوبة لعناصر JSON. لتسهيل الأمر، يستبدل المحرك مجموعة من أنواع JSON البسيطة بالمجموعة التالية:

* Nullable
* Nullable
* Nullable
* Nullable
* String

يتعرف المحرك تلقائيًا على قيم الأنواع الإضافية بناءً على تمثيلاتها بتنسيق JSON.

لتجاوز السلوك الافتراضي لتحميل بيانات JSON، قم بتهيئة وتمرير[`JsonDataLoadOptions`](../jsondataloadoptions/) instance إلى مُنشئ هذه الفئة.

## أمثلة

يوضح كيفية استخدام JSON كمصدر بيانات (سلسلة).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"},
    AlwaysGenerateRootObject = true,
    PreserveSpaces = true,
    SimpleValueParseMode = JsonSimpleValueParseMode.Loose
};

JsonDataSource dataSource = new JsonDataSource(MyDir + "List of people.json", options);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataString.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)
