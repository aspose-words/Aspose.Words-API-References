---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words för .NET
description: Lås upp kraften i Aspose.Words.Metered-klassen! Hantera enkelt din mätta nyckel med effektiva metoder för sömlös dokumentbehandling.
type: docs
weight: 4850
url: /sv/net/aspose.words/metered/
---
## Metered class

Tillhandahåller metoder för att ställa in mätad nyckel.

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
| [GetProductName](../../aspose.words/metered/getproductname/)() | Returer Produktnamn |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Ställer in uppmätt publik och privat nyckel. Om du köper en uppmätt licens bör detta API anropas när du startar applikationen, normalt räcker detta. Om det dock alltid misslyckas med att ladda upp förbrukningsdata och det tar mer än 24 timmar kommer licensen att ställas in på utvärderingsstatus. För att undvika sådana fall bör du regelbundet kontrollera licensstatusen. Om det är utvärderingsstatus, anropa detta API igen. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Får konsumtionskredit |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Hämtar förbrukningsfilens storlek |
| static [IsMeteredLicensed](../../aspose.words/metered/ismeteredlicensed/)() | Kontrollera om den mätta enheten är licensierad |

## Exempel

I det här exemplet kommer ett försök att ställa in uppmätta offentliga och privata nycklar.

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
