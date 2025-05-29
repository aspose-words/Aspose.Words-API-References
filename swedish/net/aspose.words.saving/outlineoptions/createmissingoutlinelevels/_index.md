---
title: OutlineOptions.CreateMissingOutlineLevels
linktitle: CreateMissingOutlineLevels
articleTitle: CreateMissingOutlineLevels
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen CreateMissingOutlineLevels i OutlineOptions förbättrar dokumentexporter genom att automatiskt generera saknade dispositionsnivåer för bättre organisation.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Hämtar eller anger ett värde som avgör om saknade dispositionsnivåer ska skapas när dokumentet exporteras.

Standardvärdet för den här egenskapen är`falsk`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

## Exempel

Visar hur man arbetar med dispositionsnivåer som inte innehåller några motsvarande rubriker när man sparar ett PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker som kan fungera som innehållsförteckningsposter för nivå 1 och 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Det utgående PDF-dokumentet kommer att innehålla en disposition, vilket är en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Om du klickar på en post i den här dispositionen kommer vi till platsen för respektive rubrik.
// Sätt egenskapen "HeadingsOutlineLevels" till "5" för att inkludera alla rubriker på nivå 5 och lägre i dispositionen.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Detta dokument innehåller rubriker på nivå 1 och 5, och inga rubriker på nivå 2, 3 och 4.
// Det utgående PDF-dokumentet kommer att behandla dispositionsnivåerna 2, 3 och 4 som "saknade".
// Sätt egenskapen "CreateMissingOutlineLevels" till "true" för att inkludera alla saknade nivåer i dispositionen,
// lämnar tomma dispositionsposter eftersom det inte finns några användbara rubriker.
// Sätt egenskapen "CreateMissingOutlineLevels" till "false" för att ignorera saknade dispositionsnivåer,
// och behandla rubrikerna för dispositionsnivå 5 som nivå 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Se även

* class [OutlineOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
