---
title: ImageSaveOptions.GraphicsQualityOptions
second_title: Aspose.Words per .NET API Reference
description: ImageSaveOptions proprietà. Permette di specificare la modalità di rendering e la qualità per il fileGraphics oggetto.
type: docs
weight: 20
url: /it/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Permette di specificare la modalità di rendering e la qualità per il fileGraphics oggetto.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

### Osservazioni

Utilizzare questa proprietà per sovrascrivere le impostazioni grafiche fornite dal motore Aspose.Words per impostazione predefinita.

Avrà effetto solo quando un documento viene salvato in un formato simile a un'immagine.

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../imagesaveoptions/)
* assemblea [Aspose.Words](../../../)


