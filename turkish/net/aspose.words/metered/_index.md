---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: .NET için Aspose.Words
description: Aspose.Words.Metered sınıfının gücünü açığa çıkarın! Sorunsuz belge işleme için verimli yöntemlerle ölçülü anahtarınızı kolayca yönetin.
type: docs
weight: 4850
url: /tr/net/aspose.words/metered/
---
## Metered class

Ölçülü anahtarı ayarlamak için yöntemler sağlar.

```csharp
public class Metered
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Metered](metered/)() | Bu sınıfın yeni bir örneğini başlatır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetProductName](../../aspose.words/metered/getproductname/)() | Ürün adını döndürür |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Ölçülü genel ve özel anahtarı ayarlar. Ölçülü lisans satın aldıysanız, uygulamayı başlattığınızda bu API çağrılmalıdır, normalde bu yeterlidir. Ancak, tüketim verilerini yüklemede her zaman başarısız olunursa ve 24 saati aşarsa, lisans değerlendirme durumuna ayarlanır, böyle bir durumu önlemek için, lisans durumunu düzenli olarak kontrol etmelisiniz, değerlendirme durumundaysa bu API'yi tekrar çağırın. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Tüketim kredisini alır |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Tüketim dosyası boyutunu alır |
| static [IsMeteredLicensed](../../aspose.words/metered/ismeteredlicensed/)() | Ölçümlü olup olmadığını kontrol edin |

## Örnekler

Bu örnekte, ölçülü genel ve özel anahtar ayarlama girişimi yapılacaktır

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

Ölçümlü lisansın nasıl etkinleştirileceğini ve kredi/tüketimin nasıl izleneceğini gösterir.

```csharp
// Yeni bir Ölçümlü lisans oluşturun ve ardından kullanım istatistiklerini yazdırın.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Aspose.Words'ü kullanarak çalıştırın ve ardından ne kadar harcadığımızı görmek için ölçülen istatistiklerimizi tekrar yazdırın.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Aspose Ölçülü Lisanslama mekanizması kullanım verilerini her seferinde satın alma sunucusuna göndermez,
// beklemeyi kullanmanız gerekiyor.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
