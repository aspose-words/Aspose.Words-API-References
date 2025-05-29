---
title: GraphicsQualityOptions.CompositingQuality
linktitle: CompositingQuality
articleTitle: CompositingQuality
second_title: Aspose.Words per .NET
description: Scopri la proprietà CompositingQuality di GraphicsQualityOptions per migliorare il rendering delle tue immagini. Ottimizza le immagini composite per una qualità visiva straordinaria!
type: docs
weight: 30
url: /it/net/aspose.words.saving/graphicsqualityoptions/compositingquality/
---
## GraphicsQualityOptions.CompositingQuality property

Ottiene o imposta la qualità di rendering delle immagini composite disegnate su questa grafica.

```csharp
public CompositingQuality? CompositingQuality { get; set; }
```

## Esempi

Mostra come impostare le opzioni di qualità del rendering durante la conversione di documenti in formati immagine.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions
{
    SmoothingMode = SmoothingMode.AntiAlias,
    TextRenderingHint = TextRenderingHint.ClearTypeGridFit,
    CompositingMode = CompositingMode.SourceOver,
    CompositingQuality = CompositingQuality.HighQuality,
    InterpolationMode = InterpolationMode.High,
    StringFormat = StringFormat.GenericTypographic
};

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
saveOptions.GraphicsQualityOptions = qualityOptions;

doc.Save(ArtifactsDir + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
```

### Guarda anche

* class [GraphicsQualityOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
