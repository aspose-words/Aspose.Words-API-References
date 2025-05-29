---
title: PdfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PdfSaveOptions SaveFormat för att enkelt spara dokument i PDF-format. Förenkla din filhantering med effektiva sparalternativ.
type: docs
weight: 300
url: /sv/net/aspose.words.saving/pdfsaveoptions/saveformat/
---
## PdfSaveOptions.SaveFormat property

Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan endast varaPdf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
