---
title: CsvDataLoadOptions
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف منشئ CsvDataLoadOptions—يمكنك تهيئته بسهولة باستخدام الإعدادات الافتراضية لتحميل البيانات بكفاءة والتكامل السلس.
type: docs
weight: 10
url: /ar/net/aspose.words.reporting/csvdataloadoptions/csvdataloadoptions/
---
## CsvDataLoadOptions() {#constructor}

يقوم بتهيئة مثيل جديد لهذه الفئة باستخدام الخيارات الافتراضية.

```csharp
public CsvDataLoadOptions()
```

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

---

## CsvDataLoadOptions(*bool*) {#constructor_1}

يقوم بتهيئة مثيل جديد لهذه الفئة مع تحديد ما إذا كانت بيانات CSV تحتوي على أسماء الأعمدة في السطر الأول.

```csharp
public CsvDataLoadOptions(bool hasHeaders)
```

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
