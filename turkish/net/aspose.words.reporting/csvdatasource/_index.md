---
title: Class CsvDataSource
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Reporting.CsvDataSource sınıf. Bir raporda kullanılacak bir CSV dosyası veya akışı verilerine erişim sağlar.
type: docs
weight: 4410
url: /tr/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Bir raporda kullanılacak bir CSV dosyası veya akışı verilerine erişim sağlar.

```csharp
public class CsvDataSource
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(Stream) | CSV verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir CSV akışından alınan verilerle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource](csvdatasource/#constructor_2)(string) | CSV verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir CSV dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource](csvdatasource/#constructor_1)(Stream, CsvDataLoadOptions) | CSV verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir CSV akışından alınan verilerle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource](csvdatasource/#constructor_3)(string, CsvDataLoadOptions) | CSV verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir CSV dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |

### Notlar

Bir rapor oluştururken ilgili dosyanın veya akışın verilerine erişmek için, bu sınıfın bir örneğini veri kaynağı olarak aşağıdakilerden birine iletin:[`ReportingEngine`](../reportingengine/) .BuildReport aşırı yükleniyor.

Şablon belgelerinde, bir`CsvDataSource` örneğe, sanki o was a gibi davranılmalıdır.DataTable örneği. Daha fazla bilgi için şablon sözdizimi referansına bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Virgülle ayrılmış değerlerin veri türleri, dize gösterimlerine göre otomatik olarak belirlenir. Yani template belgelerinde sadece dizeler yerine yazılan değerlerle çalışabilirsiniz. Motor, aşağıdaki türlerin değerlerini otomatik olarak tanıyabilir:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Veri türlerinin otomatik olarak tanınmasının çalışması için, virgülle ayrılmış değerlerin dize temsillerinin değişmez kültür ayarları kullanılarak oluşturulması gerektiğini unutmayın.

CSV veri yüklemesinin varsayılan davranışını geçersiz kılmak için, bir[`CsvDataLoadOptions`](../csvdataloadoptions/)instance bu sınıfın bir yapıcısına.

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)


