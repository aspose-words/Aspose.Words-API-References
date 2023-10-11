---
title: Metered.SetMeteredKey
second_title: Aspose.Words for .NET API Referansı
description: Metered yöntem. Ölçülü genel ve özel anahtarı ayarlar. Ölçülü lisans satın aldıysanız uygulamayı başlattığınızda bu APInin çağrılması gerekir normalde bu yeterlidir. Bununla birlikte tüketim verilerinin yüklenmesinde her zaman başarısız olunması ve 24 saatin aşılması durumunda lisans değerlendirme durumuna ayarlanacaktır böyle bir durumu önlemek için lisans durumunu düzenli olarak kontrol etmelisiniz değerlendirme durumu ise bu APIyi tekrar çağırın.
type: docs
weight: 20
url: /tr/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Ölçülü genel ve özel anahtarı ayarlar. Ölçülü lisans satın aldıysanız uygulamayı başlattığınızda bu API'nin çağrılması gerekir, normalde bu yeterlidir. Bununla birlikte, tüketim verilerinin yüklenmesinde her zaman başarısız olunması ve 24 saatin aşılması durumunda, lisans değerlendirme durumuna ayarlanacaktır, böyle bir durumu önlemek için, lisans durumunu düzenli olarak kontrol etmelisiniz, değerlendirme durumu ise bu API'yi tekrar çağırın.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| publicKey | String | Genel anahtar |
| privateKey | String | Özel anahtar |

### Örnekler

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

* class [Metered](../)
* ad alanı [Aspose.Words](../../metered/)
* toplantı [Aspose.Words](../../../)


