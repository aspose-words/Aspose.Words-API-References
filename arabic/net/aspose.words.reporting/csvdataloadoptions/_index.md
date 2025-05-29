---
title: CsvDataLoadOptions Class
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Reporting.CsvDataLoadOptions لتحليل بيانات CSV بكفاءة. حسّن معالجة مستنداتك مع خيارات قابلة للتخصيص اليوم!
type: docs
weight: 5400
url: /ar/net/aspose.words.reporting/csvdataloadoptions/
---
## CsvDataLoadOptions class

يمثل خيارات تحليل بيانات CSV.

لمعرفة المزيد، قم بزيارة[محرك إعداد التقارير LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) مقالة توثيقية.

```csharp
public class CsvDataLoadOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor)() | يقوم بتهيئة مثيل جديد لهذه الفئة باستخدام الخيارات الافتراضية. |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor_1)(*bool*) | يقوم بتهيئة مثيل جديد لهذه الفئة مع تحديد ما إذا كانت بيانات CSV تحتوي على أسماء الأعمدة في السطر الأول. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CommentChar](../../aspose.words.reporting/csvdataloadoptions/commentchar/) { get; set; } | يحصل على الحرف المستخدم للتعليق على أسطر بيانات CSV أو يعينه. |
| [Delimiter](../../aspose.words.reporting/csvdataloadoptions/delimiter/) { get; set; } | يحصل على الحرف الذي سيتم استخدامه كفاصل للعمود أو يعينه. |
| [HasHeaders](../../aspose.words.reporting/csvdataloadoptions/hasheaders/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان السجل الأول لبيانات CSV يحتوي على أسماء الأعمدة. |
| [QuoteChar](../../aspose.words.reporting/csvdataloadoptions/quotechar/) { get; set; } | يحصل على الحرف المستخدم لاقتباس قيم الحقول أو يعينه. |

## ملاحظات

يمكن تمرير مثيل لهذه الفئة إلى منشئي[`CsvDataSource`](../csvdatasource/) .

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
