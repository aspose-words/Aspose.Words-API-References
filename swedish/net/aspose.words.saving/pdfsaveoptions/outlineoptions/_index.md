---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words för .NET
description: Upptäck PdfSaveOptions OutlineOptions-egenskap för att enkelt anpassa dina PDF-konturer. Förbättra navigeringen och förbättra dokumentets användbarhet!
type: docs
weight: 240
url: /sv/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Gör det möjligt att ange dispositionsalternativ.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Anmärkningar

Konturer kan skapas från rubriker och bokmärken.

För rubriker bestäms dispositionsnivån av rubriknivån.

Det är möjligt att ställa in den maximala rubriknivån som ska inkluderas i konturer eller inaktivera rubrikkonturer helt och hållet.

För bokmärken kan dispositionsnivån anges i alternativen som ett standardvärde för alla bokmärken eller som individuella värden för specifika bokmärken.

Även konturer kan exporteras till XPS-format med hjälp av samma`OutlineOptions` klass.

## Exempel

Visar hur man begränsar rubriknivån som visas i konturen i ett sparat PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker som kan fungera som innehållsförteckningsposter för nivå 1, 2 och sedan 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Det utgående PDF-dokumentet kommer att innehålla en disposition, vilket är en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Om du klickar på en post i den här dispositionen kommer vi till platsen för respektive rubrik.
// Sätt egenskapen "HeadingsOutlineLevels" till "2" för att exkludera alla rubriker vars nivåer är över 2 från dispositionen.
// De två sista rubrikerna som vi har infogat ovan kommer inte att visas.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

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

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
