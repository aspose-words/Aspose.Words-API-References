---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: Aspose.Words för .NET
description: Hantera enkelt din uppmätta licens med SetMeteredKey-metoden. Säkerställ sömlösa datauppladdningar och undvik utvärderingsstatus med regelbundna kontroller.
type: docs
weight: 30
url: /sv/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Ställer in uppmätt publik och privat nyckel. Om du köper en uppmätt licens bör detta API anropas när du startar applikationen, normalt räcker detta. Om det dock alltid misslyckas med att ladda upp förbrukningsdata och det tar mer än 24 timmar kommer licensen att ställas in på utvärderingsstatus. För att undvika sådana fall bör du regelbundet kontrollera licensstatusen. Om det är utvärderingsstatus, anropa detta API igen.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| publicKey | String | offentlig nyckel |
| privateKey | String | privat nyckel |

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
