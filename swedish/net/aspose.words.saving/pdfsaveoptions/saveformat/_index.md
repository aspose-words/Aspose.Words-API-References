---
title: PdfSaveOptions.SaveFormat
second_title: Aspose.Words för .NET API Referens
description: PdfSaveOptions fast egendom. Anger formatet som dokumentet kommer att sparas i om detta sparaalternativobjekt används. Kan endastPdf .
type: docs
weight: 250
url: /sv/net/aspose.words.saving/pdfsaveoptions/saveformat/
---
## PdfSaveOptions.SaveFormat property

Anger formatet som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan endastPdf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../pdfsaveoptions/)
* hopsättning [Aspose.Words](../../../)


