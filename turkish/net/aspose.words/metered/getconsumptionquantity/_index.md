---
title: Metered.GetConsumptionQuantity
second_title: Aspose.Words for .NET API Referansı
description: Metered yöntem. Tüketim dosyasının boyutunu alır
type: docs
weight: 40
url: /tr/net/aspose.words/metered/getconsumptionquantity/
---
## Metered.GetConsumptionQuantity method

Tüketim dosyasının boyutunu alır

```csharp
public static decimal GetConsumptionQuantity()
```

### Geri dönüş değeri

tüketim miktarı

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


