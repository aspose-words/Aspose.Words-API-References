---
title: Metered.GetConsumptionQuantity
second_title: Aspose.Words for .NET API Referansı
description: Metered yöntem. size tüketim dosyası alır
type: docs
weight: 40
url: /tr/net/aspose.words/metered/getconsumptionquantity/
---
## Metered.GetConsumptionQuantity method

size tüketim dosyası alır

```csharp
public static decimal GetConsumptionQuantity()
```

### Geri dönüş değeri

tüketim miktarı

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


