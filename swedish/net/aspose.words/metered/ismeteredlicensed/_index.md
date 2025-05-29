---
title: Metered.IsMeteredLicensed
linktitle: IsMeteredLicensed
articleTitle: IsMeteredLicensed
second_title: Aspose.Words för .NET
description: Ta reda på om din mätmetod är licensierad med IsMetered. Säkerställ efterlevnad och dra nytta av fördelarna med licensierade tjänster idag!
type: docs
weight: 60
url: /sv/net/aspose.words/metered/ismeteredlicensed/
---
## Metered.IsMeteredLicensed method

Kontrollera om den mätta enheten är licensierad

```csharp
public static bool IsMeteredLicensed()
```

### Returvärde

Sant eller falskt

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
