---
title: JsonDataSource
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words لـ .NET
description: قم بإنشاء مصدر بيانات قوي بسهولة باستخدام منشئ JsonDataSource، مما يتيح التكامل السلس لملفات JSON وتحليل البيانات بشكل محسن.
type: docs
weight: 10
url: /ar/net/aspose.words.reporting/jsondatasource/jsondatasource/
---
## JsonDataSource(*string*) {#constructor_2}

ينشئ مصدر بيانات جديد بالبيانات من ملف JSON باستخدام الخيارات الافتراضية لتحليل بيانات JSON.

```csharp
public JsonDataSource(string jsonPath)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| jsonPath | String | المسار إلى ملف JSON الذي سيتم استخدامه كمصدر للبيانات. |

### أنظر أيضا

* class [JsonDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## JsonDataSource(*Stream*) {#constructor}

ينشئ مصدر بيانات جديد بالبيانات من مجرى JSON باستخدام الخيارات الافتراضية لتحليل بيانات JSON.

```csharp
public JsonDataSource(Stream jsonStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| jsonStream | Stream | تدفق بيانات JSON الذي سيتم استخدامه كمصدر للبيانات. |

### أنظر أيضا

* class [JsonDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## JsonDataSource(*string, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_3}

ينشئ مصدر بيانات جديد بالبيانات من ملف JSON باستخدام الخيارات المحددة لتحليل بيانات JSON.

```csharp
public JsonDataSource(string jsonPath, JsonDataLoadOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| jsonPath | String | المسار إلى ملف JSON الذي سيتم استخدامه كمصدر للبيانات. |
| options | JsonDataLoadOptions | خيارات لتحليل بيانات JSON. |

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

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## JsonDataSource(*Stream, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_1}

ينشئ مصدر بيانات جديد بالبيانات من مجرى JSON باستخدام الخيارات المحددة لتحليل بيانات JSON.

```csharp
public JsonDataSource(Stream jsonStream, JsonDataLoadOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| jsonStream | Stream | تدفق بيانات JSON الذي سيتم استخدامه كمصدر للبيانات. |
| options | JsonDataLoadOptions | خيارات لتحليل بيانات JSON. |

## أمثلة

يوضح كيفية استخدام JSON كمصدر بيانات (دفق).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"}
};

using (FileStream stream = File.OpenRead(MyDir + "List of people.json"))
{
    JsonDataSource dataSource = new JsonDataSource(stream, options);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataStream.docx");
```

### أنظر أيضا

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
