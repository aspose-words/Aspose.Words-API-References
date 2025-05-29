---
title: PdfSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words för .NET
description: Upptäck PdfSaveOptions Clone-metoden för att enkelt skapa en djup klon av dina objekt och förbättra dina PDF-hanteringsmöjligheter.
type: docs
weight: 370
url: /sv/net/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions.Clone method

Skapar en djup klon av detta objekt.

```csharp
public PdfSaveOptions Clone()
```

## Exempel

Visar hur man uppdaterar alla fält i ett dokument omedelbart innan det sparas som PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga text med fälten PAGE och NUMPAGES. Dessa fält visar inte rätt värde i realtid.
// Vi måste uppdatera dem manuellt med hjälp av uppdateringsmetoder som "Field.Update()" och "Document.UpdateFields()"
// varje gång vi behöver dem för att visa korrekta värden.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Sätt egenskapen "UpdateFields" till "false" för att inte uppdatera alla fält i ett dokument precis innan en sparningsåtgärd.
// Detta är det bästa alternativet om vi vet att alla våra fält kommer att vara uppdaterade innan vi sparar.
// Sätt egenskapen "UpdateFields" till "true" för att iterera genom hela dokumentet
// fält och uppdatera dem innan vi sparar det som en PDF. Detta säkerställer att alla fält visas
// de mest exakta värdena i PDF-filen.
options.UpdateFields = updateFields;

// Vi kan klona PdfSaveOptions-objekt.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
