---
title: ImageSaveOptions.VerticalResolution
linktitle: VerticalResolution
articleTitle: VerticalResolution
second_title: Aspose.Words per .NET
description: Scopri la proprietà VerticalResolution di ImageSaveOptions per impostare e ottimizzare facilmente la qualità dell'immagine in DPI per immagini straordinarie. Migliora i tuoi progetti oggi stesso!
type: docs
weight: 200
url: /it/net/aspose.words.saving/imagesaveoptions/verticalresolution/
---
## ImageSaveOptions.VerticalResolution property

Ottiene o imposta la risoluzione verticale per le immagini generate, in punti per pollice.

```csharp
public float VerticalResolution { get; set; }
```

## Osservazioni

Questa proprietà ha effetto solo quando si salva in formati di immagini raster e influenza la dimensione di output in pixel.

Il valore predefinito è 96.

## Esempi

Mostra come modificare l'immagine mentre Aspose.Words converte un documento in un'immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// modifica l'immagine mentre l'operazione di salvataggio la esegue.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Possiamo regolare queste proprietà per cambiare la luminosità e il contrasto dell'immagine.
    // Entrambi sono su una scala da 0 a 1 e per impostazione predefinita sono impostati su 0,5.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Possiamo regolare la risoluzione orizzontale e verticale con queste proprietà.
    // Ciò influirà sulle dimensioni dell'immagine.
    // Il valore predefinito per queste proprietà è 96,0, per una risoluzione di 96 dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Possiamo ridimensionare l'immagine usando questa proprietà. Il valore predefinito è 1,0, per un ridimensionamento del 100%.
    // Possiamo usare questa proprietà per annullare qualsiasi modifica alle dimensioni dell'immagine causata dalla modifica della risoluzione.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Guarda anche

* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
