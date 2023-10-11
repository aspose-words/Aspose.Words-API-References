---
title: Class XmlDataSource
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Reporting.XmlDataSource sınıf. Bir raporda kullanılacak XML dosyası veya akışının verilerine erişim sağlar.
type: docs
weight: 4750
url: /tr/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Bir raporda kullanılacak XML dosyası veya akışının verilerine erişim sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[LINQ Raporlama Motoru](https://docs.aspose.com/words/net/linq-reporting-engine/) dokümantasyon makalesi.

```csharp
public class XmlDataSource
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(Stream) | XML veri yüklemesi için varsayılan seçenekleri kullanarak XML akışından gelen verilerle yeni bir veri kaynağı oluşturur. |
| [XmlDataSource](xmldatasource/#constructor_4)(string) | XML veri yüklemesi için varsayılan seçenekleri kullanarak XML dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |
| [XmlDataSource](xmldatasource/#constructor_2)(Stream, Stream) | XML Şema Tanımı akışını kullanarak XML akışındaki verilerle yeni bir veri kaynağı oluşturur. XML verilerinin yüklenmesi için varsayılan options kullanılır. |
| [XmlDataSource](xmldatasource/#constructor_1)(Stream, XmlDataLoadOptions) | XML veri yüklemesi için belirtilen seçenekleri kullanarak XML akışındaki verilerle yeni bir veri kaynağı oluşturur. |
| [XmlDataSource](xmldatasource/#constructor_6)(string, string) | XML Şema Tanımı dosyasını kullanarak XML dosyasındaki verilerle yeni bir veri kaynağı oluşturur. XML verilerinin yüklenmesi için varsayılan options kullanılır. |
| [XmlDataSource](xmldatasource/#constructor_5)(string, XmlDataLoadOptions) | XML veri yüklemesi için belirtilen seçenekleri kullanarak XML dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |
| [XmlDataSource](xmldatasource/#constructor_3)(Stream, Stream, XmlDataLoadOptions) | XML Şema Tanımı akışını kullanarak XML akışındaki verilerle yeni bir veri kaynağı oluşturur. Belirtilen seçenekleri XML veri yüklemesi için kullanılır. |
| [XmlDataSource](xmldatasource/#constructor_7)(string, string, XmlDataLoadOptions) | XML Şema Tanımı dosyasını kullanarak XML dosyasındaki verilerle yeni bir veri kaynağı oluşturur. Belirtilen seçenekleri XML veri yüklemesi için kullanılır. |

### Notlar

Bir rapor oluştururken ilgili dosyanın veya akışın verilerine erişmek için, bu sınıfın bir örneğini as veri kaynağı olarak aşağıdakilerden birine iletin.[`ReportingEngine`](../reportingengine/) .BuildReport aşırı yüklemeleri.

Şablon belgelerinde, üst düzey bir XML öğesi yalnızca aynı türdeki öğelerin bir listesini içeriyorsa, an`XmlDataSource` örnek sanki aymış gibi ele alınmalıdır.DataTable örneği. Aksi takdirde, bir`XmlDataSource` örnek sanki aymış gibi ele alınmalıdır.DataRow örneği. Daha fazla bilgi için şablon söz dizimi referansına bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

XML Şema Tanımı bu sınıfın yapıcısına iletildiğinde, basit XML elemanlarının değerlerinin veri türleri ve öznitelikler şemaya göre belirlenir. Yani şablon belgelerinde yalnızca dizeler yerine yazılan değerlerle çalışabilirsiniz.

XML Şeması Tanımı bu sınıfın yapıcısına aktarılmadığında, basit XML öğelerinin değerlerinin veri türleri ve nitelikleri dize gösterimlerine göre otomatik olarak belirlenir. Yani şablon belgelerde, bu durumda da ile yazılan değerlerle çalışabilirsiniz. Motor aşağıdaki türlerdeki değerleri otomatik olarak tanıyabilir:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Veri türlerinin otomatik olarak tanınmasının çalışması için, basit XML öğelerinin ( ) değerlerinin dize temsillerinin ve niteliklerin değişmez kültür ayarları kullanılarak oluşturulması gerektiğini unutmayın.

XML veri yüklemesinin varsayılan davranışını geçersiz kılmak için, bir başlangıç değeri oluşturun ve iletin[`XmlDataLoadOptions`](../xmldataloadoptions/) örneğini bu sınıfın yapıcısına.

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)


