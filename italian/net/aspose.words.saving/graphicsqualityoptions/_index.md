---
title: Class GraphicsQualityOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.GraphicsQualityOptions classe. Permette di specificare ulterioriGraphics opzioni di qualità.
type: docs
weight: 5040
url: /it/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Permette di specificare ulterioriGraphics opzioni di qualità.

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

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
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Ottiene o imposta un valore che specifica il modo in cui le immagini composte vengono disegnate in questo Graphics. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Ottiene o imposta la qualità di rendering delle immagini composte disegnate in questo Graphics. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Ottiene o imposta la modalità di interpolazione associata a questo Graphics. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Ottiene o imposta la qualità di rendering per questa grafica. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Ottiene o imposta informazioni sul layout del testo (come allineamento, orientamento e punti di tabulazione), manipolazioni di visualizzazione (come inserimento di puntini di sospensione e sostituzione di cifre nazionali) e funzionalità OpenType. |
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


