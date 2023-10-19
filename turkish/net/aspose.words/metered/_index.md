---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words for .NET
description: Aspose.Words.Metered sınıf. Ölçülü anahtarı ayarlamak için yöntemler sağlar C#'da.
type: docs
weight: 4160
url: /tr/net/aspose.words/metered/
---
## Metered class

Ölçülü anahtarı ayarlamak için yöntemler sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Lisanslama ve Abonelik](https://docs.aspose.com/words/net/licensing/) dokümantasyon makalesi.

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
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Ölçülü genel ve özel anahtarı ayarlar. Ölçülü lisans satın aldıysanız uygulamayı başlattığınızda bu API'nin çağrılması gerekir, normalde bu yeterlidir. Bununla birlikte, tüketim verilerinin yüklenmesinde her zaman başarısız olunması ve 24 saatin aşılması durumunda, lisans değerlendirme durumuna ayarlanacaktır, böyle bir durumu önlemek için, lisans durumunu düzenli olarak kontrol etmelisiniz, değerlendirme durumu ise bu API'yi tekrar çağırın. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Tüketim kredisi alır |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Tüketim dosyasının boyutunu alır |

## Örnekler

Bu örnekte, ölçülü genel ve özel anahtar ayarlanmaya çalışılacaktır

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

Ölçülü lisansın nasıl etkinleştirileceğini ve kredinin/tüketimin nasıl izleneceğini gösterir.

```csharp
// Yeni bir Ölçülü lisans oluşturun ve ardından kullanım istatistiklerini yazdırın.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Aspose.Words'ü kullanarak çalıştırın ve ne kadar harcadığımızı görmek için ölçümlü istatistiklerimizi tekrar yazdırın.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Aspose Ölçülü Lisanslama mekanizması her seferinde kullanım verilerini satın alma sunucusuna göndermez,
//beklemeyi kullanmanız gerekiyor.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
