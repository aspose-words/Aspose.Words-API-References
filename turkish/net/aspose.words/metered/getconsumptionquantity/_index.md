---
title: Metered.GetConsumptionQuantity
linktitle: GetConsumptionQuantity
articleTitle: GetConsumptionQuantity
second_title: .NET için Aspose.Words
description: Dosya boyutu verilerini verimli bir şekilde almak ve kaynak yönetiminizi optimize etmek için Metered GetConsumptionQuantity yöntemini keşfedin. Veri içgörülerinizi geliştirin!
type: docs
weight: 50
url: /tr/net/aspose.words/metered/getconsumptionquantity/
---
## Metered.GetConsumptionQuantity method

Tüketim dosyası boyutunu alır

```csharp
public static decimal GetConsumptionQuantity()
```

### Geri dönüş değeri

tüketim miktarı

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
