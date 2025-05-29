---
title: JsonDataLoadOptions
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف منشئ JsonDataLoadOptions، وقم بتهيئة تحميل البيانات الخاصة بك بسهولة باستخدام إعدادات افتراضية قابلة للتخصيص للحصول على الأداء الأمثل.
type: docs
weight: 10
url: /ar/net/aspose.words.reporting/jsondataloadoptions/jsondataloadoptions/
---
## JsonDataLoadOptions constructor

يقوم بتهيئة مثيل جديد لهذه الفئة باستخدام الخيارات الافتراضية.

```csharp
public JsonDataLoadOptions()
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

* class [JsonDataLoadOptions](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
