---
title: WatermarkerContext.TextWatermark
linktitle: TextWatermark
articleTitle: TextWatermark
second_title: Aspose.Words för .NET
description: Upptäck funktionen WatermarkerContext TextWatermark för att enkelt lägga till anpassningsbara textvattenmärken, vilket förbättrar ditt innehålls säkerhet och varumärke.
type: docs
weight: 40
url: /sv/net/aspose.words.lowcode/watermarkercontext/textwatermark/
---
## WatermarkerContext.TextWatermark property

Text som ska användas som vattenstämpel.

```csharp
public string TextWatermark { get; set; }
```

## Anmärkningar

Om båda[`ImageWatermark`](../imagewatermark/) och`TextWatermark` anges, åsidosätter textvattenmärke bildvattenmärke.

## Exempel

Visar hur man infogar vattenstämpeltext i dokumentet med hjälp av kontext.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.TextWatermark = watermarkText;

watermarkerContext.TextWatermarkOptions.Color = Color.Red;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextText.docx")
    .Execute();
```

Visar hur man infogar vattenstämpeltext i dokumentet från strömmen med hjälp av kontext.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.TextWatermark = watermarkText;

    watermarkerContext.TextWatermarkOptions.Color = Color.Red;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextTextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Se även

* class [WatermarkerContext](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
