---
title: PdfSaveOptions.OutlineOptions
second_title: Aspose.Words för .NET API Referens
description: PdfSaveOptions fast egendom. Gör det möjligt att ange konturalternativ.
type: docs
weight: 210
url: /sv/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Gör det möjligt att ange konturalternativ.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Anmärkningar

Konturer kan skapas från rubriker och bokmärken.

För rubriker bestäms dispositionsnivån av rubriknivån.

Det är möjligt att ställa in den maximala rubriknivån som ska inkluderas i konturer eller inaktivera rubrikkonturer överhuvudtaget.

För bokmärken kan dispositionsnivå ställas in i alternativen som ett standardvärde för alla bokmärken eller som individuella värden för särskilda bokmärken.

Konturer kan också exporteras till XPS-format genom att använda samma`OutlineOptions` klass.

### Exempel

Visar hur man begränsar rubrikernas nivå som kommer att visas i konturerna av ett sparat PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker som kan fungera som TOC-poster på nivåerna 1, 2 och sedan 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Det utgående PDF-dokumentet kommer att innehålla en disposition, som är en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Genom att klicka på en post i denna disposition kommer vi till platsen för dess respektive rubrik.
// Ställ in egenskapen "HeadingsOutlineLevels" till "2" för att utesluta alla rubriker vars nivåer är över 2 från dispositionen.
// De två sista rubrikerna vi har infogat ovan kommer inte att visas.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

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

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../pdfsaveoptions/)
* hopsättning [Aspose.Words](../../../)


