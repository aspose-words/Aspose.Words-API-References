---
title: Metered.Metered
second_title: Aspose.Words for .NET API Referansı
description: Metered inşaatçı. Bu sınıfın yeni bir örneğini başlatır.
type: docs
weight: 10
url: /tr/net/aspose.words/metered/metered/
---
## Metered constructor

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public Metered()
```

### Örnekler

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

* class [Metered](../)
* ad alanı [Aspose.Words](../../metered/)
* toplantı [Aspose.Words](../../../)


