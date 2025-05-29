---
title: GraphicsQualityOptions Class
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.GraphicsQualityOptions per migliorare la qualità della grafica dei documenti con opzioni personalizzabili per un output di qualità superiore.
type: docs
weight: 5790
url: /it/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Consente di specificare ulterioriGraphics opzioni di qualità.

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
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Ottiene o imposta un valore che specifica come le immagini composte vengono disegnate in questa grafica. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Ottiene o imposta la qualità di rendering delle immagini composite disegnate su questa grafica. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Ottiene o imposta la modalità di interpolazione associata a questa grafica. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Ottiene o imposta la qualità di rendering per questa grafica. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Ottiene o imposta le informazioni sul layout del testo (ad esempio allineamento, orientamento e tabulazioni), le manipolazioni della visualizzazione (ad esempio l'inserimento di ellissi e la sostituzione delle cifre nazionali) e le funzionalità OpenType. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | Ottiene o imposta la modalità di rendering per il testo associato a questa grafica. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | Ottiene o imposta un flag che indica se WrapMode è TileFlipXY. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
