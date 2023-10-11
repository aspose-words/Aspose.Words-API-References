---
title: Class JsonDataSource
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Reporting.JsonDataSource sınıf. Bir raporda kullanılacak JSON dosyası veya akışına ait verilere erişim sağlar.
type: docs
weight: 4690
url: /tr/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Bir raporda kullanılacak JSON dosyası veya akışına ait verilere erişim sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[LINQ Raporlama Motoru](https://docs.aspose.com/words/net/linq-reporting-engine/) dokümantasyon makalesi.

```csharp
public class JsonDataSource
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(Stream) | JSON verilerini ayrıştırmaya yönelik varsayılan seçenekleri kullanarak bir JSON akışından gelen verilerle yeni bir veri kaynağı oluşturur. |
| [JsonDataSource](jsondatasource/#constructor_2)(string) | JSON verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir JSON dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |
| [JsonDataSource](jsondatasource/#constructor_1)(Stream, JsonDataLoadOptions) | JSON verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir JSON akışından gelen verilerle yeni bir veri kaynağı oluşturur. |
| [JsonDataSource](jsondatasource/#constructor_3)(string, JsonDataLoadOptions) | JSON verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir JSON dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |

### Notlar

Bir rapor oluştururken ilgili dosyanın veya akışın verilerine erişmek için, bu sınıfın bir örneğini as veri kaynağı olarak aşağıdakilerden birine iletin.[`ReportingEngine`](../reportingengine/) .BuildReport aşırı yüklemeleri.

Şablon belgelerinde, üst düzey bir JSON öğesi bir diziyse,`JsonDataSource` örneğine sanki bir örnekmiş gibi davranılmalıdır.DataTable örneği. Üst düzey JSON öğesi bir nesneyse,`JsonDataSource` örnek sanki aymış gibi ele alınmalıdır.DataRow örneği. Daha fazla bilgi için şablon söz dizimi referansına bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Şablon belgelerde, JSON öğelerinin yazılan değerleriyle çalışabilirsiniz. Kolaylık sağlamak için motor, JSON basit türlerinin kümesini aşağıdakiyle değiştirir:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Motor, ekstra türlerin değerlerini JSON temsillerine göre otomatik olarak tanır.

JSON veri yüklemesinin varsayılan davranışını geçersiz kılmak için, bir başlangıç değeri oluşturun ve iletin[`JsonDataLoadOptions`](../jsondataloadoptions/) example bu sınıfın yapıcısına.

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)


