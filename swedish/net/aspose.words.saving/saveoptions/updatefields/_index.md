---
title: SaveOptions.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words för .NET
description: SaveOptions UpdateFields fast egendom. Hämtar eller ställer in ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen ärSann  i C#.
type: docs
weight: 160
url: /sv/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Hämtar eller ställer in ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är`Sann` .

```csharp
public bool UpdateFields { get; set; }
```

## Anmärkningar

Gör det möjligt att ange om MS Word-beteende ska härma eller inte.

## Exempel

Visar hur du uppdaterar alla fält i ett dokument direkt innan du sparar det till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga text med PAGE- och NUMPAGES-fälten. Dessa fält visar inte det korrekta värdet i realtid.
// Vi kommer att behöva uppdatera dem manuellt med uppdateringsmetoder som "Field.Update()" och "Document.UpdateFields()"
// varje gång vi behöver dem för att visa korrekta värden.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in "UpdateFields"-egenskapen till "false" för att inte uppdatera alla fält i ett dokument precis innan en spara-operation.
// Detta är det bästa alternativet om vi vet att alla våra fält kommer att vara uppdaterade innan vi sparar.
// Ställ in egenskapen "UpdateFields" till "true" för att iterera genom hela dokumentet
//-fält och uppdatera dem innan vi sparar det som en PDF. Detta kommer att se till att alla fält visas
// de mest exakta värdena i PDF:en.
options.UpdateFields = updateFields;

// Vi kan klona PdfSaveOptions-objekt.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
