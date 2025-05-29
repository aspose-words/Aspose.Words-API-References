---
title: WatermarkerContext.ImageWatermark
linktitle: ImageWatermark
articleTitle: ImageWatermark
second_title: Aspose.Words för .NET
description: Upptäck hur du kan förbättra dina bilder med egenskapen WatermarkerContext ImageWatermark, så att du enkelt kan lägga till anpassade vattenstämpelbilder.
type: docs
weight: 20
url: /sv/net/aspose.words.lowcode/watermarkercontext/imagewatermark/
---
## WatermarkerContext.ImageWatermark property

Bildbyte som ska användas som vattenstämpel.

```csharp
public byte[] ImageWatermark { get; set; }
```

## Anmärkningar

Om båda`ImageWatermark` och[`TextWatermark`](../textwatermark/) anges, åsidosätter textvattenmärke bildvattenmärke.

## Exempel

Visar hur man infogar en vattenstämpelbild i dokumentet med hjälp av kontext.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

watermarkerContext.ImageWatermarkOptions.Scale = 50;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextImage.docx")
    .Execute();
```

Visar hur man infogar en vattenstämpelbild i dokumentet från en ström med hjälp av kontext.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

    watermarkerContext.ImageWatermarkOptions.Scale = 50;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextImageStream.docx", FileMode.Create, FileAccess.ReadWrite))
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
