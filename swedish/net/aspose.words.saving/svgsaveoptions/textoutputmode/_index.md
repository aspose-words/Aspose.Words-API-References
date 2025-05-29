---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SvgSaveOptions TextOutputMode, som styr textrendering i SVG för förbättrad visuell kvalitet och anpassningsmöjligheter. Optimera din grafik idag!
type: docs
weight: 120
url: /sv/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Hämtar eller anger ett värde som avgör hur text ska renderas i SVG.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Anmärkningar

Använd den här egenskapen för att hämta eller ange läget för hur text i ett dokument ska renderas när det sparas i SVG-format.

Standardvärdet ärUseTargetMachineFonts.

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

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
