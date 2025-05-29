---
title: JsonDataLoadOptions.AlwaysGenerateRootObject
linktitle: AlwaysGenerateRootObject
articleTitle: AlwaysGenerateRootObject
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية JsonDataLoadOptions AlwaysGenerateRootObject على تعزيز معالجة بيانات JSON من خلال ضمان كائن جذر متسق للتكامل السلس.
type: docs
weight: 20
url: /ar/net/aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/
---
## JsonDataLoadOptions.AlwaysGenerateRootObject property

يحصل على أو يضبط علامة تشير إلى ما إذا كان مصدر البيانات المُولّد سيحتوي دائمًا على كائن لعنصر JSON root . إذا كان عنصر JSON root يحتوي على خاصية معقدة واحدة، فلن يتم إنشاء هذا الكائن افتراضيًا.

```csharp
public bool AlwaysGenerateRootObject { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

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

* class [JsonDataLoadOptions](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
