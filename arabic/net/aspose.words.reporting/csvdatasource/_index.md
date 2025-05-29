---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words لـ .NET
description: تمتع بالوصول إلى بيانات CSV واستخدامها بسهولة مع Aspose.Words.Reporting.CsvDataSource. حسّن تقاريرك بتكامل بيانات سلس!
type: docs
weight: 5410
url: /ar/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

يوفر الوصول إلى بيانات ملف CSV أو التدفق الذي سيتم استخدامه داخل التقرير.

لمعرفة المزيد، قم بزيارة[محرك إعداد التقارير LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) مقالة توثيقية.

```csharp
public class CsvDataSource
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | ينشئ مصدر بيانات جديد باستخدام البيانات من دفق CSV باستخدام الخيارات الافتراضية لتحليل بيانات CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | ينشئ مصدر بيانات جديد باستخدام البيانات من ملف CSV باستخدام الخيارات الافتراضية لتحليل بيانات CSV. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | ينشئ مصدر بيانات جديد باستخدام البيانات من مجرى CSV باستخدام الخيارات المحددة لتحليل بيانات CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | ينشئ مصدر بيانات جديد باستخدام البيانات من ملف CSV باستخدام الخيارات المحددة لتحليل بيانات CSV. |

## ملاحظات

للوصول إلى بيانات الملف أو التدفق المقابل أثناء إنشاء تقرير، مرر مثيلًا لهذه الفئة as مصدر بيانات إلى أحد[`ReportingEngine`](../reportingengine/) .BuildReport overloads.

في مستندات القالب، أ`CsvDataSource` يجب التعامل مع المثيل بنفس الطريقة كما لو كان aDataTableمثال . لمزيد من المعلومات، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

يتم تحديد أنواع بيانات القيم المفصولة بفواصل تلقائيًا بناءً على تمثيلاتها النصية. لذا، في مستندات template ، يمكنك العمل مع القيم المكتوبة بدلًا من السلاسل النصية فقط. يستطيع المحرك التعرف تلقائيًا على قيم من الأنواع التالية:

* Nullable
* Nullable
* Nullable
* Nullable
* String

لاحظ أنه لكي يعمل التعرف التلقائي على أنواع البيانات، يجب تشكيل تمثيلات سلسلة من القيم المنفصلة بفاصلة باستخدام إعدادات الثقافة الثابتة.

لتجاوز السلوك الافتراضي لتحميل بيانات CSV، قم بتهيئة وتمرير[`CsvDataLoadOptions`](../csvdataloadoptions/) instance إلى مُنشئ هذه الفئة.

## أمثلة

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)
