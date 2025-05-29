---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen SvgSaveOptions FitToViewPort optimerar din SVG-utdata för att perfekt fylla alla webbläsarfönster eller behållare för fantastiska bilder.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Anger om utdata-SVG-filen ska fylla det tillgängliga visningsområdet (webbläsarfönster eller container). När den är inställd på`sann`Bredd och höjd på utdata-SVG är inställda på 100 %.

Standardvärdet är`falsk`.

```csharp
public bool FitToViewPort { get; set; }
```

## Exempel

Visar hur man efterliknar bilders egenskaper när man konverterar ett .docx-dokument till .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Konfigurera SvgSaveOptions-objektet för att spara utan sidkantlinjer eller valbar text.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Se även

* class [SvgSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
