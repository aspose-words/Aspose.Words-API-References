---
title: JsonDataLoadOptions.AlwaysGenerateRootObject
linktitle: AlwaysGenerateRootObject
articleTitle: AlwaysGenerateRootObject
second_title: .NET için Aspose.Words
description: JsonDataLoadOptions AlwaysGenerateRootObject özelliğinin, sorunsuz entegrasyon için tutarlı bir kök nesne sağlayarak JSON veri işlemenizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/
---
## JsonDataLoadOptions.AlwaysGenerateRootObject property

Oluşturulan bir veri kaynağının her zaman bir JSON root öğesi için bir nesne içerip içermeyeceğini belirten bir bayrak alır veya ayarlar. Bir JSON kök öğesi tek bir karmaşık özellik içeriyorsa, böyle bir nesne varsayılan olarak oluşturulmaz.

```csharp
public bool AlwaysGenerateRootObject { get; set; }
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
