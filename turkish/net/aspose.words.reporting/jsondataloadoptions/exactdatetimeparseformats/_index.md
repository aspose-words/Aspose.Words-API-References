---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: .NET için Aspose.Words
description: Kesin JSON tarih-saat ayrıştırması için JsonDataLoadOptions' ExactDateTimeParseFormats'ı keşfedin. Sorunsuz veri yüklemesi için biçimleri kolayca özelleştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

JSON yüklenirken JSON tarih-saat değerlerinin ayrıştırılması için kesin biçimleri alır veya ayarlar. Varsayılan değer`hükümsüz` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Notlar

Microsoft® JSON tarih-saat biçimini kullanarak kodlanan dizeler (örneğin, "/Date(1224043200000)/") her zaman bu özelliğin bir değerinden bağımsız olarak tarih-saat değerleri olarak tanınır. Özellik, tarih-saat değerlerini dizelerden ayrıştırırken kullanılacak ek biçimlerini şu şekilde tanımlar:

* Ne zaman`ExactDateTimeParseFormats` dır`hükümsüz` , ISO-8601 biçimi ve güncel, İngilizce ABD ve İngilizce Yeni Zelanda kültürleri için desteklenen tüm tarih-saat biçimleri ayrıca belirtilen sırayla kullanılır.
* Ne zaman`ExactDateTimeParseFormats`dizeler içerir, bunlar geçerli kültürü kullanan ek date-time biçimleri olarak kullanılır.
* Ne zaman`ExactDateTimeParseFormats` boşsa, ek tarih-saat biçimleri kullanılmaz.

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
