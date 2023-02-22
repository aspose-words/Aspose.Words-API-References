---
title: Class JsonDataSource
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Reporting.JsonDataSource sınıf. Bir rapor içinde kullanılacak bir JSON dosyası veya akışının verilerine erişim sağlar.
type: docs
weight: 4430
url: /tr/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Bir rapor içinde kullanılacak bir JSON dosyası veya akışının verilerine erişim sağlar.

```csharp
public class JsonDataSource
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(Stream) | JSON verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir JSON akışından alınan verilerle yeni bir veri kaynağı oluşturur. |
| [JsonDataSource](jsondatasource/#constructor_2)(string) | JSON verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir JSON dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |
| [JsonDataSource](jsondatasource/#constructor_1)(Stream, JsonDataLoadOptions) | JSON verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir JSON akışındaki verilerle yeni bir veri kaynağı oluşturur. |
| [JsonDataSource](jsondatasource/#constructor_3)(string, JsonDataLoadOptions) | JSON verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir JSON dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |

### Notlar

Bir rapor oluştururken ilgili dosyanın veya akışın verilerine erişmek için, bu sınıfın bir örneğini veri kaynağı olarak aşağıdakilerden birine iletin:[`ReportingEngine`](../reportingengine/) .BuildReport aşırı yükleniyor.

Şablon belgelerinde, bir üst düzey JSON öğesi bir diziyse,`JsonDataSource` örneğine , sanki bir örnekmiş gibi davranılmalıdır.DataTable örneği. Bir üst düzey JSON öğesi bir nesneyse,`JsonDataSource` örneğe a olduğu gibi davranılmalıdırDataRow örneği. Daha fazla bilgi için şablon sözdizimi referansına bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Şablon belgelerinde, JSON öğelerinin yazılan değerleriyle çalışabilirsiniz. Kolaylık sağlamak için motor, JSON basit türlerinin kümesini aşağıdakiyle değiştirir:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Motor, JSON temsillerine göre ekstra türlerin değerlerini otomatik olarak tanır.

JSON veri yüklemesinin varsayılan davranışını geçersiz kılmak için, bir[`JsonDataLoadOptions`](../jsondataloadoptions/)instance bu sınıfın bir yapıcısına.

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)


