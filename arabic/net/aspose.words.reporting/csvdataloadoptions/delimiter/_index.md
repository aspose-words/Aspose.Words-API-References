---
title: CsvDataLoadOptions.Delimiter
linktitle: Delimiter
articleTitle: Delimiter
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CsvDataLoadOptions Delimiter لتخصيص فواصل الأعمدة بسهولة لضمان تحميل بيانات أكثر كفاءة. حسّن إدارة بياناتك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words.reporting/csvdataloadoptions/delimiter/
---
## CsvDataLoadOptions.Delimiter property

يحصل على الحرف الذي سيتم استخدامه كفاصل للعمود أو يعينه.

```csharp
public char Delimiter { get; set; }
```

## ملاحظات

القيمة الافتراضية هي ',' (فاصلة).

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

* class [CsvDataLoadOptions](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
