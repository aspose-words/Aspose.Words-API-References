---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: .NET için Aspose.Words
description: Aspose.Words.Reporting.CsvDataSource ile CSV verilerine zahmetsizce erişin ve kullanın. Raporlarınızı kusursuz veri entegrasyonuyla geliştirin!
type: docs
weight: 5410
url: /tr/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Bir rapor içerisinde kullanılacak bir CSV dosyası veya akışının verilerine erişim sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[LINQ Raporlama Motoru](https://docs.aspose.com/words/net/linq-reporting-engine/) belgeleme makalesi.

```csharp
public class CsvDataSource
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | CSV verilerini ayrıştırmak için varsayılan seçenekleri kullanarak CSV akışından gelen verilerle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | CSV verilerini ayrıştırmak için varsayılan seçenekleri kullanarak CSV dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | CSV verilerini ayrıştırmak için belirtilen seçenekleri kullanarak CSV akışından gelen verilerle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | CSV verilerini ayrıştırmak için belirtilen seçenekleri kullanarak CSV dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |

## Notlar

Bir rapor oluştururken ilgili dosyanın veya akışın verilerine erişmek için, bu sınıfın bir örneğini bir veri kaynağı olarak aşağıdakilere geçirin:[`ReportingEngine`](../reportingengine/) .BuildReport aşırı yüklemeleri.

Şablon belgelerinde,`CsvDataSource` örnek, sanki bir şeymiş gibi ele alınmalıdırDataTable örneği. Daha fazla bilgi için şablon sözdizimi başvurusu 'ye bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Virgülle ayrılmış değerlerin veri türleri, dize gösterimlerine göre otomatik olarak belirlenir. Bu nedenle template belgelerinde, yalnızca dizeler yerine yazılmış değerlerle çalışabilirsiniz. Motor, aşağıdaki türlerdeki değerlerini otomatik olarak tanıyabilir:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Veri türlerinin otomatik olarak tanınması için, virgülle ayrılmış değerlerin dize gösterimlerinin değişmez kültür ayarları kullanılarak oluşturulması gerektiğini unutmayın.

CSV veri yüklemesinin varsayılan davranışını geçersiz kılmak için bir[`CsvDataLoadOptions`](../csvdataloadoptions/) instance bu sınıfın bir kurucusuna.

## Örnekler

CSV'nin veri kaynağı (dize) olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)
