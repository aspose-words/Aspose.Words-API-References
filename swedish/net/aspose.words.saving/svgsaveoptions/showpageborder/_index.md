---
title: SvgSaveOptions.ShowPageBorder
linktitle: ShowPageBorder
articleTitle: ShowPageBorder
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SvgSaveOptions ShowPageBorder för att anpassa din sidkontur. Kontrollera kantlinjer enkelt – standardinställningen är sann för enkel användning!
type: docs
weight: 110
url: /sv/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Styr om en kantlinje läggs till i sidans kontur. Standard är`sann` .

```csharp
public bool ShowPageBorder { get; set; }
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
