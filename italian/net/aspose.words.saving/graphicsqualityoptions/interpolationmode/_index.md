---
title: GraphicsQualityOptions.InterpolationMode
second_title: Aspose.Words per .NET API Reference
description: GraphicsQualityOptions proprietà. Ottiene o imposta la modalità di interpolazione associata a questa grafica.
type: docs
weight: 40
url: /it/net/aspose.words.saving/graphicsqualityoptions/interpolationmode/
---
## GraphicsQualityOptions.InterpolationMode property

Ottiene o imposta la modalità di interpolazione associata a questa grafica.

```csharp
public InterpolationMode? InterpolationMode { get; set; }
```

### Esempi

Mostra come impostare le opzioni di qualità di rendering durante la conversione di documenti in formati immagine.

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
* spazio dei nomi [Aspose.Words.Saving](../../graphicsqualityoptions/)
* assemblea [Aspose.Words](../../../)


