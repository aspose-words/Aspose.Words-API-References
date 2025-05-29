---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Reporting.JsonDataLoadOptions لتحليل بيانات JSON بسلاسة. حسّن معالجة مستنداتك بخيارات مرنة!
type: docs
weight: 5420
url: /ar/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

يمثل خيارات تحليل بيانات JSON.

لمعرفة المزيد، قم بزيارة[محرك إعداد التقارير LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) مقالة توثيقية.

```csharp
public class JsonDataLoadOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | يقوم بتهيئة مثيل جديد لهذه الفئة باستخدام الخيارات الافتراضية. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | يحصل على أو يضبط علامة تشير إلى ما إذا كان مصدر البيانات المُولّد سيحتوي دائمًا على كائن لعنصر JSON root . إذا كان عنصر JSON root يحتوي على خاصية معقدة واحدة، فلن يتم إنشاء هذا الكائن افتراضيًا. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | يحصل على أو يضبط التنسيقات الدقيقة لتحليل قيم التاريخ والوقت JSON أثناء تحميل JSON. الإعداد الافتراضي هو`باطل` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | يحصل على أو يعين علمًا يشير إلى ما إذا كان يجب الحفاظ على المسافات البادئة واللاحقة عند تحميل قيم string لبيانات JSON. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | يحصل على أو يضبط وضعًا لتحليل قيم JSON البسيطة (null، وboolean، وnumber، وinteger، وstring) أثناء تحميل JSON. لا يؤثر هذا الوضع على تحليل قيم التاريخ والوقت. الوضع الافتراضي هو Loose . |

## ملاحظات

يمكن تمرير مثيل لهذه الفئة إلى منشئي[`JsonDataSource`](../jsondatasource/) .

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
