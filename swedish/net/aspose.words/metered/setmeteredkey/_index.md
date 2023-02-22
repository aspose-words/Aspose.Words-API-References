---
title: Metered.SetMeteredKey
second_title: Aspose.Words för .NET API Referens
description: Metered metod. Ställer in mätt offentlig och privat nyckel. Om du köper mätlicens när du startar applikationen bör detta API anropas normalt räcker detta. Men om alltid misslyckas med att ladda upp förbrukningsdata och överskrider 24 timmar kommer licensen att ställas in på utvärderingsstatus för att undvika sådana fall bör du regelbundet kontrollera licensstatusen om det är utvärderingsstatus ring detta API igen.
type: docs
weight: 20
url: /sv/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Ställer in mätt offentlig och privat nyckel. Om du köper mätlicens, när du startar applikationen, bör detta API anropas, normalt räcker detta. Men om alltid misslyckas med att ladda upp förbrukningsdata och överskrider 24 timmar, kommer licensen att ställas in på utvärderingsstatus, för att undvika sådana fall bör du regelbundet kontrollera licensstatusen, om det är utvärderingsstatus, ring detta API igen.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| publicKey | String | offentlig nyckel |
| privateKey | String | privat nyckel |

### Exempel

Visar hur du aktiverar en mätlicens och spårar kredit/förbrukning.

```csharp
// Skapa en ny Metered-licens och skriv sedan ut dess användningsstatistik.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Använd Aspose.Words och skriv sedan ut vår mätstatistik igen för att se hur mycket vi spenderade.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Aspose Metered Licensing-mekanism skickar inte användningsdata till köpservern varje gång,
// du måste använda väntande.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Se även

* class [Metered](../)
* namnutrymme [Aspose.Words](../../metered/)
* hopsättning [Aspose.Words](../../../)


