---
title: Metered.GetConsumptionQuantity
linktitle: GetConsumptionQuantity
articleTitle: GetConsumptionQuantity
second_title: Aspose.Words för .NET
description: Upptäck metoden Metered GetConsumptionQuantity för att effektivt hämta filstorleksdata och optimera din resurshantering. Förbättra dina datainsikter!
type: docs
weight: 50
url: /sv/net/aspose.words/metered/getconsumptionquantity/
---
## Metered.GetConsumptionQuantity method

Hämtar förbrukningsfilens storlek

```csharp
public static decimal GetConsumptionQuantity()
```

### Returvärde

förbrukningsmängd

## Exempel

Visar hur man aktiverar en mätt licens och spårar kredit/förbrukning.

```csharp
// Skapa en ny mätt licens och skriv sedan ut dess användningsstatistik.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Använd Aspose.Words och skriv sedan ut vår mätstatistik igen för att se hur mycket vi spenderade.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Aspose Metered Licensing-mekanism skickar inte användningsdata till köpservern varje gång,
// du måste använda väntan.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Se även

* class [Metered](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
