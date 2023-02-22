---
title: Class GraphicsQualityOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.GraphicsQualityOptions classe. Consente di specificare ulterioriGraphics opzioni di qualità.
type: docs
weight: 4780
url: /it/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Consente di specificare ulterioriGraphics opzioni di qualità.

```csharp
public class GraphicsQualityOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [GraphicsQualityOptions](graphicsqualityoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Ottiene o imposta un valore che specifica il modo in cui le immagini composte vengono disegnate in questa grafica. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Ottiene o imposta la qualità di rendering delle immagini composte disegnate su questa grafica. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Ottiene o imposta la modalità di interpolazione associata a questa grafica. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Ottiene o imposta la qualità di rendering per questa grafica. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Ottiene o imposta le informazioni sul layout del testo (come allineamento, orientamento e tabulazioni), le manipolazioni di visualizzazione (come l'inserimento di puntini di sospensione e la sostituzione di cifre nazionali) e le funzioni OpenType. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | Ottiene o imposta la modalità di rendering per il testo associato a questa grafica. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | Ottiene o imposta un flag che indica se WrapMode è TileFlipXY. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


