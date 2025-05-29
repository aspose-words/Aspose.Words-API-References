---
title: GraphicsQualityOptions.CompositingMode
linktitle: CompositingMode
articleTitle: CompositingMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà CompositingMode di GraphicsQualityOptions per ottimizzare il rendering delle immagini, migliorando così la qualità e le prestazioni della tua grafica.
type: docs
weight: 20
url: /it/net/aspose.words.saving/graphicsqualityoptions/compositingmode/
---
## GraphicsQualityOptions.CompositingMode property

Ottiene o imposta un valore che specifica come le immagini composte vengono disegnate in questa grafica.

```csharp
public CompositingMode? CompositingMode { get; set; }
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
