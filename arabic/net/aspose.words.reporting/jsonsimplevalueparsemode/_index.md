---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Reporting.JsonSimpleValueParseMode لتحليل JSON بكفاءة. تعامل بسهولة مع القيم الفارغة، والقيم المنطقية، والأرقام، والسلاسل النصية بسلاسة!
type: docs
weight: 5440
url: /ar/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

يحدد وضعًا لتحليل قيم JSON البسيطة (null، وboolean، وnumber، وinteger، وstring) أثناء تحميل JSON. لا يؤثر هذا الوضع على تحليل قيم التاريخ والوقت.

```csharp
public enum JsonSimpleValueParseMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Loose | `0` | يحدد الوضع الذي يتم فيه تحديد أنواع قيم JSON البسيطة عند تحليل تمثيلاتها النصية. على سبيل المثال، يتم تحديد نوع 'prop' من مقتطف JSON '{ prop: "123" }' كعدد صحيح في هذا الوضع. |
| Strict | `1` | يحدد الوضع الذي يتم فيه تحديد أنواع قيم JSON البسيطة من تدوين JSON نفسه. على سبيل المثال، يتم تحديد نوع 'prop' من مقتطف JSON '{ prop: "123" }' كسلسلة في هذا الوضع. |

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
