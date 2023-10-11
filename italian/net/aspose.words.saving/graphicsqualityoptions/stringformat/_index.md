---
title: GraphicsQualityOptions.StringFormat
second_title: Aspose.Words per .NET API Reference
description: GraphicsQualityOptions proprietà. Ottiene o imposta informazioni sul layout del testo come allineamento orientamento e punti di tabulazione manipolazioni di visualizzazione come inserimento di puntini di sospensione e sostituzione di cifre nazionali e funzionalità OpenType.
type: docs
weight: 60
url: /it/net/aspose.words.saving/graphicsqualityoptions/stringformat/
---
## GraphicsQualityOptions.StringFormat property

Ottiene o imposta informazioni sul layout del testo (come allineamento, orientamento e punti di tabulazione), manipolazioni di visualizzazione (come inserimento di puntini di sospensione e sostituzione di cifre nazionali) e funzionalità OpenType.

```csharp
public StringFormat StringFormat { get; set; }
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


