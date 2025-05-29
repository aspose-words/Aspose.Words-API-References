---
title: JsonDataLoadOptions.PreserveSpaces
linktitle: PreserveSpaces
articleTitle: PreserveSpaces
second_title: .NET için Aspose.Words
description: JsonDataLoadOptions PreserveSpaces özelliğinin, doğru dize değerleri için öndeki ve sondaki boşlukları koruyarak JSON veri işlemeyi nasıl geliştirdiğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.reporting/jsondataloadoptions/preservespaces/
---
## JsonDataLoadOptions.PreserveSpaces property

JSON verilerinin string değerleri yüklenirken öndeki ve arkadaki boşlukların korunup korunmayacağını belirten bir bayrak alır veya ayarlar.

```csharp
public bool PreserveSpaces { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

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

* class [JsonDataLoadOptions](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
