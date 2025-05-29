---
title: CsvDataSource
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words لـ .NET
description: أنشئ مصدر بيانات CSV قويًا بسهولة باستخدام مُنشئ مصدر بيانات CsvDataSource. بسّط تحليل البيانات باستخدام الخيارات الافتراضية لضمان تكامل سلس.
type: docs
weight: 10
url: /ar/net/aspose.words.reporting/csvdatasource/csvdatasource/
---
## CsvDataSource(*string*) {#constructor_2}

ينشئ مصدر بيانات جديد باستخدام البيانات من ملف CSV باستخدام الخيارات الافتراضية لتحليل بيانات CSV.

```csharp
public CsvDataSource(string csvPath)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| csvPath | String | المسار إلى ملف CSV الذي سيتم استخدامه كمصدر للبيانات. |

### أنظر أيضا

* class [CsvDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## CsvDataSource(*string, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_3}

ينشئ مصدر بيانات جديد باستخدام البيانات من ملف CSV باستخدام الخيارات المحددة لتحليل بيانات CSV.

```csharp
public CsvDataSource(string csvPath, CsvDataLoadOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| csvPath | String | المسار إلى ملف CSV الذي سيتم استخدامه كمصدر للبيانات. |
| options | CsvDataLoadOptions | خيارات لتحليل بيانات CSV. |

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

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## CsvDataSource(*Stream*) {#constructor}

ينشئ مصدر بيانات جديد باستخدام البيانات من دفق CSV باستخدام الخيارات الافتراضية لتحليل بيانات CSV.

```csharp
public CsvDataSource(Stream csvStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| csvStream | Stream | تدفق بيانات CSV الذي سيتم استخدامه كمصدر للبيانات. |

### أنظر أيضا

* class [CsvDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## CsvDataSource(*Stream, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_1}

ينشئ مصدر بيانات جديد باستخدام البيانات من مجرى CSV باستخدام الخيارات المحددة لتحليل بيانات CSV.

```csharp
public CsvDataSource(Stream csvStream, CsvDataLoadOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| csvStream | Stream | تدفق بيانات CSV الذي سيتم استخدامه كمصدر للبيانات. |
| options | CsvDataLoadOptions | خيارات لتحليل بيانات CSV. |

## أمثلة

يوضح كيفية استخدام CSV كمصدر بيانات (دفق).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';

using (FileStream stream = File.OpenRead(MyDir + "List of people.csv"))
{
    CsvDataSource dataSource = new CsvDataSource(stream, loadOptions);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataStream.docx");
```

### أنظر أيضا

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
