---
title: Metered
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words for .NET
description: Metered inşaatçı. Bu sınıfın yeni bir örneğini başlatır C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/metered/metered/
---
## Metered constructor

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public Metered()
```

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
