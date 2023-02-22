---
title: OutlineOptions.CreateMissingOutlineLevels
second_title: Aspose.Words för .NET API Referens
description: OutlineOptions fast egendom. Hämtar eller ställer in ett värde som bestämmer om saknade dispositionsnivåer ska skapas eller inte när dokumentet exporteras.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Hämtar eller ställer in ett värde som bestämmer om saknade dispositionsnivåer ska skapas eller inte när dokumentet exporteras.

Standardvärdet för den här egenskapen är **falsk**.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

### Exempel

Visar hur man arbetar med dispositionsnivåer som inte innehåller några motsvarande rubriker när man sparar ett PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker som kan fungera som TOC-poster på nivå 1 och 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Det utgående PDF-dokumentet kommer att innehålla en disposition, som är en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Genom att klicka på en post i denna disposition kommer vi till platsen för dess respektive rubrik.
// Ställ in "HeadingsOutlineLevels"-egenskapen till "5" för att inkludera alla rubriker på nivå 5 och lägre i dispositionen.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

  // Detta dokument innehåller rubriker på nivåerna 1 och 5, och inga rubriker med nivåerna 2, 3 och 4.
// PDF-dokumentet kommer att behandla dispositionsnivåerna 2, 3 och 4 som "saknas".
// Ställ in egenskapen "CreateMissingOutlineLevels" till "true" för att inkludera alla saknade nivåer i dispositionen,
// lämnar tomma konturposter eftersom det inte finns några användbara rubriker.
// Ställ in egenskapen "CreateMissingOutlineLevels" till "false" för att ignorera saknade dispositionsnivåer,
// och behandla rubrikerna på nivå 5 som nivå 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Se även

* class [OutlineOptions](../)
* namnutrymme [Aspose.Words.Saving](../../outlineoptions/)
* hopsättning [Aspose.Words](../../../)


