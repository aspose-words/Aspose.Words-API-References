---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: .NET için Aspose.Words
description: Kusursuz JSON veri ayrıştırma için Aspose.Words.Reporting.JsonDataLoadOptions sınıfını keşfedin. Esnek seçeneklerle belge işlemenizi geliştirin!
type: docs
weight: 5420
url: /tr/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

JSON verilerini ayrıştırma seçeneklerini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[LINQ Raporlama Motoru](https://docs.aspose.com/words/net/linq-reporting-engine/) belgeleme makalesi.

```csharp
public class JsonDataLoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | Bu sınıfın yeni bir örneğini varsayılan seçeneklerle başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Oluşturulan bir veri kaynağının her zaman bir JSON root öğesi için bir nesne içerip içermeyeceğini belirten bir bayrak alır veya ayarlar. Bir JSON kök öğesi tek bir karmaşık özellik içeriyorsa, böyle bir nesne varsayılan olarak oluşturulmaz. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | JSON yüklenirken JSON tarih-saat değerlerinin ayrıştırılması için kesin biçimleri alır veya ayarlar. Varsayılan değer`hükümsüz` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | JSON verilerinin string değerleri yüklenirken öndeki ve arkadaki boşlukların korunup korunmayacağını belirten bir bayrak alır veya ayarlar. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | JSON yüklenirken JSON basit değerlerini (null, boolean, sayı, tam sayı ve dize) ayrıştırmak için bir mod alır veya ayarlar . Böyle bir mod tarih-saat değerlerinin ayrıştırılmasını etkilemez. Varsayılan 'dirLoose . |

## Notlar

Bu sınıfın bir örneği, kurucularına geçirilebilir[`JsonDataSource`](../jsondatasource/) .

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
