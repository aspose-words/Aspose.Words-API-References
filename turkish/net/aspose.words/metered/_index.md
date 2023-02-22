---
title: Class Metered
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Metered sınıf. Ölçülen anahtarı ayarlamak için yöntemler sağlar.
type: docs
weight: 3920
url: /tr/net/aspose.words/metered/
---
## Metered class

Ölçülen anahtarı ayarlamak için yöntemler sağlar.

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
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(string, string) | Ölçülü genel ve özel anahtarı ayarlar. Ölçülü lisans satın alırsanız, uygulamayı başlattığınızda bu API çağrılmalıdır, normalde bu yeterlidir. Ancak, tüketim verileri her zaman yüklenemezse ve 24 saati aşarsa, lisans değerlendirme durumuna ayarlanır, böyle bir durumdan kaçınmak için , lisans durumunu düzenli olarak kontrol etmelisiniz, eğer değerlendirme durumuysa bu API'yi tekrar arayın. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Tüketim kredisi alır |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | size tüketim dosyası alır |

### Örnekler

Bu örnekte, ölçülen genel ve özel anahtarın ayarlanması denenecektir

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

Sayaçlı bir lisansın nasıl etkinleştirileceğini ve kredi/tüketimin nasıl izleneceğini gösterir.

```csharp
// Yeni bir Sayaçlı lisans oluşturun ve ardından kullanım istatistiklerini yazdırın.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Aspose.Words kullanarak çalıştırın ve ardından ne kadar harcadığımızı görmek için ölçülen istatistiklerimizi tekrar yazdırın.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Aspose Metered Licensing mekanizması kullanım verilerini her seferinde satın alma sunucusuna göndermez,
// beklemeyi kullanmanız gerekiyor.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


