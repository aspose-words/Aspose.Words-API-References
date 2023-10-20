---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words för .NET
description: Aspose.Words.Metered klass. Tillhandahåller metoder för att ställa in mätnyckel i C#.
type: docs
weight: 4160
url: /sv/net/aspose.words/metered/
---
## Metered class

Tillhandahåller metoder för att ställa in mätnyckel.

För att lära dig mer, besök[Licensiering och prenumeration](https://docs.aspose.com/words/net/licensing/) dokumentationsartikel.

```csharp
public class Metered
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Metered](metered/)() | Initierar en ny instans av den här klassen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Ställer in mätt offentlig och privat nyckel. Om du köper mätlicens, när du startar applikationen, bör detta API anropas, normalt räcker detta. Men om alltid misslyckas med att ladda upp förbrukningsdata och överskrider 24 timmar, kommer licensen att ställas in på utvärderingsstatus, för att undvika sådana fall bör du regelbundet kontrollera licensstatusen, om det är utvärderingsstatus, ring detta API igen. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Får konsumtionskredit |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Får förbrukningsfilstorlek |

## Exempel

I det här exemplet kommer ett försök att göras att ställa in mätt offentlig och privat nyckel

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
