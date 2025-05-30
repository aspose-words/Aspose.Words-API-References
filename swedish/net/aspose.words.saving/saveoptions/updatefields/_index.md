---
title: SaveOptions.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen SaveOptions UpdateFields optimerar dokumentsparning genom att uppdatera specifika fälttyper innan de konverteras till fasta format. Standardvärde sant.
type: docs
weight: 170
url: /sv/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Hämtar eller anger ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är`sann` .

```csharp
public bool UpdateFields { get; set; }
```

## Anmärkningar

Gör det möjligt att ange om beteendet i MS Word ska efterliknas eller inte.

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

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
