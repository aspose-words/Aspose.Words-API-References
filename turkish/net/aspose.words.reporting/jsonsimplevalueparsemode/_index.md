---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: .NET için Aspose.Words
description: Verimli JSON ayrıştırma için Aspose.Words.Reporting.JsonSimpleValueParseMode enum'unu keşfedin. Null'ları, boole'ları, sayıları ve dizeleri sorunsuz bir şekilde kolayca işleyin!
type: docs
weight: 5440
url: /tr/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

JSON yüklenirken JSON basit değerlerinin (null, boolean, sayı, tam sayı ve dize) ayrıştırılması için bir mod belirtir. Böyle bir mod tarih-saat değerlerinin ayrıştırılmasını etkilemez.

```csharp
public enum JsonSimpleValueParseMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Loose | `0` | JSON basit değerlerinin türlerinin dize gösterimlerinin ayrıştırılmasıyla belirlendiği modu belirtir. Örneğin, JSON parçacığı '{ prop: "123" }'deki 'prop' türü bu modda tamsayı olarak belirlenir. |
| Strict | `1` | JSON basit değerlerinin türlerinin JSON gösteriminden belirlendiği modu belirtir. Örneğin, JSON parçacığı '{ prop: "123" }'daki 'prop' türü bu modda dize olarak belirlenir. |

## Örnekler

JSON'un veri kaynağı (dize) olarak nasıl kullanılacağını gösterir.

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

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)
