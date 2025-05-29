---
title: CsvDataLoadOptions.QuoteChar
linktitle: QuoteChar
articleTitle: QuoteChar
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية QuoteChar الخاصة بـ CsvDataLoadOptions لتخصيص قيمة الحقل بسهولة للتعامل مع البيانات بسلاسة وتحسين إدارة CSV.
type: docs
weight: 50
url: /ar/net/aspose.words.reporting/csvdataloadoptions/quotechar/
---
## CsvDataLoadOptions.QuoteChar property

يحصل على الحرف المستخدم لاقتباس قيم الحقول أو يعينه.

```csharp
public char QuoteChar { get; set; }
```

## ملاحظات

القيمة الافتراضية هي '"' (علامة اقتباس).

قم بمضاعفة الحرف لوضعه في النص المقتبس.

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
