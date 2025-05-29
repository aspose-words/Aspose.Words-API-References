---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: .NET için Aspose.Words
description: SetMeteredKey yöntemi ile ölçümlü lisansınızı zahmetsizce yönetin. Düzenli kontrollerle sorunsuz veri yüklemelerini sağlayın ve değerlendirme durumundan kaçının.
type: docs
weight: 30
url: /tr/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Ölçülü genel ve özel anahtarı ayarlar. Ölçülü lisans satın aldıysanız, uygulamayı başlattığınızda bu API çağrılmalıdır, normalde bu yeterlidir. Ancak, tüketim verilerini yüklemede her zaman başarısız olunursa ve 24 saati aşarsa, lisans değerlendirme durumuna ayarlanır, böyle bir durumu önlemek için, lisans durumunu düzenli olarak kontrol etmelisiniz, değerlendirme durumundaysa bu API'yi tekrar çağırın.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| publicKey | String | genel anahtar |
| privateKey | String | özel anahtar |

## Örnekler

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

* class [Metered](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
