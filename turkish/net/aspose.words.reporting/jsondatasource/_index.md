---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: .NET için Aspose.Words
description: Aspose.Words.Reporting.JsonDataSource ile güçlü raporlamanın kilidini açın. Raporlarınıza sorunsuz entegrasyon için JSON verilerine kolayca erişin.
type: docs
weight: 5430
url: /tr/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Bir rapor içerisinde kullanılacak bir JSON dosyasının veya akışının verilerine erişim sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[LINQ Raporlama Motoru](https://docs.aspose.com/words/net/linq-reporting-engine/) belgeleme makalesi.

```csharp
public class JsonDataSource
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | JSON verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir JSON akışından gelen verilerle yeni bir veri kaynağı oluşturur. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | JSON verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir JSON dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | JSON verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir JSON akışından gelen verilerle yeni bir veri kaynağı oluşturur. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | JSON verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir JSON dosyasından gelen verilerle yeni bir veri kaynağı oluşturur. |

## Notlar

Bir rapor oluştururken ilgili dosyanın veya akışın verilerine erişmek için, bu sınıfın bir örneğini bir veri kaynağı olarak aşağıdakilere geçirin:[`ReportingEngine`](../reportingengine/) .BuildReport aşırı yüklemeleri.

Şablon belgelerinde, en üst düzey JSON öğesi bir diziyse,`JsonDataSource` örnek, bir gibi aynı şekilde ele alınmalıdırDataTable örneği. En üst düzey JSON öğesi bir nesneyse,`JsonDataSource` örnek, bir örnekmiş gibi ele alınmalıdırDataRow örneği. Daha fazla bilgi için şablon sözdizimi başvurusu 'ye bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Şablon belgelerinde, JSON öğelerinin yazılmış değerleriyle çalışabilirsiniz. Kolaylık olması açısından, motor JSON basit türlerinin kümesini aşağıdakiyle değiştirir:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Motor, ekstra tiplerin değerlerini JSON gösterimlerine göre otomatik olarak tanır.

JSON veri yüklemesinin varsayılan davranışını geçersiz kılmak için bir[`JsonDataLoadOptions`](../jsondataloadoptions/) instance bu sınıfın bir kurucusuna.

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
