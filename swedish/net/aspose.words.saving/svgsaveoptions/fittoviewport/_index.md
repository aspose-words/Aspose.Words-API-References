---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words för .NET
description: SvgSaveOptions FitToViewPort fast egendom. Anger om utdata SVG ska fylla det tillgängliga visningsområdet webbläsarfönster eller behållare. När inställt påSann bredd och höjd på utdata SVG är inställda på 100 i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Anger om utdata SVG ska fylla det tillgängliga visningsområdet (webbläsarfönster eller behållare). När inställt på`Sann` bredd och höjd på utdata SVG är inställda på 100%.

Standardvärdet är`falsk`.

```csharp
public bool FitToViewPort { get; set; }
```

## Exempel

Visar hur man efterliknar egenskaperna hos bilder när man konverterar ett .docx-dokument till .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Konfigurera SvgSaveOptions-objektet för att spara utan sidkanter eller valbar text.
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
