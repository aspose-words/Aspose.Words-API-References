---
title: OutlineOptions.ExpandedOutlineLevels
linktitle: ExpandedOutlineLevels
articleTitle: ExpandedOutlineLevels
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ExpandedOutlineLevels i OutlineOptions, som låter dig anpassa dokumentdispositionernas synlighet för förbättrad navigering och användarupplevelse.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/outlineoptions/expandedoutlinelevels/
---
## OutlineOptions.ExpandedOutlineLevels property

Anger hur många nivåer i dokumentdispositionen som ska visas expanderad när filen visas.

```csharp
public int ExpandedOutlineLevels { get; set; }
```

## Anmärkningar

Observera att dessa alternativ inte fungerar när du sparar till XPS.

Ange 0 så hopfälls dokumentets disposition; ange 1 så expanderas de första nivåerna items i dispositionen och så vidare.

Standardvärdet är 0. Giltigt intervall är 0 till 9.

## Exempel

Visar hur man konverterar ett helt dokument till PDF med tre nivåer i dokumentdispositionen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker för nivå 1 till 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Det utgående PDF-dokumentet kommer att innehålla en disposition, vilket är en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Om du klickar på en post i den här dispositionen kommer vi till platsen för respektive rubrik.
// Sätt egenskapen "HeadingsOutlineLevels" till "4" för att exkludera alla rubriker vars nivåer är över 4 från dispositionen.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Om en dispositionspost har efterföljande poster på en högre nivå mellan sig själv och nästa post på samma eller lägre nivå,
// en pil visas till vänster om posten. Denna post är "ägare" till flera sådana "underposter".
// I vårt dokument är dispositionsposterna från den 5:e rubriknivån underposter till den andra dispositionsposten på den 4:e nivån,
// posterna på rubriknivå 4 och 5 är underposter till den andra posten på nivå 3, och så vidare.
// I dispositionen kan vi klicka på pilen för posten "ägare" för att minimera/expandera alla dess underposter.
// Sätt egenskapen "ExpandedOutlineLevels" till "2" för att automatiskt expandera alla rubriknivå 2 och lägre dispositionsposter
// och komprimerar alla poster på nivå 3 och högre när vi öppnar dokumentet.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Se även

* class [OutlineOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
