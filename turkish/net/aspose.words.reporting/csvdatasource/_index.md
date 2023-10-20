---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words for .NET
description: Aspose.Words.Reporting.CsvDataSource sınıf. Bir raporda kullanılacak CSV dosyası veya akış verilerine erişim sağlar C#'da.
type: docs
weight: 4670
url: /tr/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Bir raporda kullanılacak CSV dosyası veya akış verilerine erişim sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[LINQ Raporlama Motoru](https://docs.aspose.com/words/net/linq-reporting-engine/) dokümantasyon makalesi.

```csharp
public class CsvDataSource
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | CSV verilerini ayrıştırmaya yönelik varsayılan seçenekleri kullanarak CSV akışındaki verilerle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | CSV verilerini ayrıştırmak için varsayılan seçenekleri kullanarak CSV dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | CSV verilerini ayrıştırmak için belirtilen seçenekleri kullanarak CSV akışından gelen verilerle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | CSV verilerini ayrıştırmak için belirtilen seçenekleri kullanarak CSV dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |

## Notlar

Bir rapor oluştururken ilgili dosyanın veya akışın verilerine erişmek için, bu sınıfın bir örneğini as veri kaynağı olarak aşağıdakilerden birine iletin.[`ReportingEngine`](../reportingengine/) .BuildReport aşırı yüklemeleri.

Şablon belgelerde, bir`CsvDataSource` örnek sanki was a gibi ele alınmalıdırDataTable örneği. Daha fazla bilgi için şablon söz dizimi referansına bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Virgülle ayrılmış değerlerin veri türleri, dize gösterimlerine göre otomatik olarak belirlenir. Yani şablon belgelerinde yalnızca dizeler yerine yazılan değerlerle çalışabilirsiniz. Motor, aşağıdaki türlerdeki değerlerini otomatik olarak tanıyabilir:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Veri türlerinin otomatik olarak tanınmasının işe yaraması için, virgülle ayrılmış değerlerin dize temsillerinin değişmez kültür ayarları kullanılarak oluşturulması gerektiğini unutmayın.

CSV veri yüklemesinin varsayılan davranışını geçersiz kılmak için, bir başlangıç değeri oluşturun ve iletin[`CsvDataLoadOptions`](../csvdataloadoptions/) example bu sınıfın yapıcısına.

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)
