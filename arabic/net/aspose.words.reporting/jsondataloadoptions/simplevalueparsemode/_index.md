---
title: JsonDataLoadOptions.SimpleValueParseMode
linktitle: SimpleValueParseMode
articleTitle: SimpleValueParseMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية SimpleValueParseMode في JsonDataLoadOptions تحليل JSON للقيم الفارغة، والقيم المنطقية، والأرقام، والسلاسل النصية. حسّن تحميل بياناتك اليوم!
type: docs
weight: 50
url: /ar/net/aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/
---
## JsonDataLoadOptions.SimpleValueParseMode property

يحصل على أو يضبط وضعًا لتحليل قيم JSON البسيطة (null، وboolean، وnumber، وinteger، وstring) أثناء تحميل JSON. لا يؤثر هذا الوضع على تحليل قيم التاريخ والوقت. الوضع الافتراضي هو Loose .

```csharp
public JsonSimpleValueParseMode SimpleValueParseMode { get; set; }
```

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

* enum [JsonSimpleValueParseMode](../../jsonsimplevalueparsemode/)
* class [JsonDataLoadOptions](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
