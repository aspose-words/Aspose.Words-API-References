---
title: Metered.GetConsumptionCredit
linktitle: GetConsumptionCredit
articleTitle: GetConsumptionCredit
second_title: Aspose.Words for .NET
description: Metered GetConsumptionCredit yöntem. Tüketim kredisi alır C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words/metered/getconsumptioncredit/
---
## Metered.GetConsumptionCredit method

Tüketim kredisi alır

```csharp
public static decimal GetConsumptionCredit()
```

### Geri dönüş değeri

tüketim miktarı

## Örnekler

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
