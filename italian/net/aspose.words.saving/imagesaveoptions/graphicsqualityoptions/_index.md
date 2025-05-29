---
title: ImageSaveOptions.GraphicsQualityOptions
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words per .NET
description: Ottimizza la tua grafica con la proprietà GraphicsQualityOptions di ImageSaveOptions, che consente modalità di rendering precise e una qualità superiore per effetti visivi straordinari.
type: docs
weight: 20
url: /it/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Consente di specificare la modalità di rendering e la qualità per ilGraphics oggetto.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

## Osservazioni

Utilizzare questa proprietà per sovrascrivere le impostazioni grafiche fornite per impostazione predefinita dal motore Aspose.Words.

Avrà effetto solo se il documento verrà salvato in un formato simile a un'immagine.

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
