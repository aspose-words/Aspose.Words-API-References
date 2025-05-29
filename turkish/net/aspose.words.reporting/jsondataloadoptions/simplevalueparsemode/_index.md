---
title: JsonDataLoadOptions.SimpleValueParseMode
linktitle: SimpleValueParseMode
articleTitle: SimpleValueParseMode
second_title: .NET için Aspose.Words
description: JsonDataLoadOptions'daki SimpleValueParseMode özelliğinin null'lar, boole'lar, sayılar ve dizeler için JSON ayrıştırmasını nasıl geliştirdiğini keşfedin. Veri yüklemenizi bugün optimize edin!
type: docs
weight: 50
url: /tr/net/aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/
---
## JsonDataLoadOptions.SimpleValueParseMode property

JSON yüklenirken JSON basit değerlerini (null, boolean, sayı, tam sayı ve dize) ayrıştırmak için bir mod alır veya ayarlar . Böyle bir mod tarih-saat değerlerinin ayrıştırılmasını etkilemez. Varsayılan 'dirLoose .

```csharp
public JsonSimpleValueParseMode SimpleValueParseMode { get; set; }
```

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

* enum [JsonSimpleValueParseMode](../../jsonsimplevalueparsemode/)
* class [JsonDataLoadOptions](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
