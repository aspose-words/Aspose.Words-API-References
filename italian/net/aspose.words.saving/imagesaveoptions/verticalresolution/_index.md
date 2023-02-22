---
title: ImageSaveOptions.VerticalResolution
second_title: Aspose.Words per .NET API Reference
description: ImageSaveOptions proprietà. Ottiene o imposta la risoluzione verticale per le immagini generate in punti per pollice.
type: docs
weight: 190
url: /it/net/aspose.words.saving/imagesaveoptions/verticalresolution/
---
## ImageSaveOptions.VerticalResolution property

Ottiene o imposta la risoluzione verticale per le immagini generate, in punti per pollice.

```csharp
public float VerticalResolution { get; set; }
```

### Osservazioni

Questa proprietà ha effetto solo durante il salvataggio in formati di immagine raster e influisce sulla dimensione dell'output in pixel.

Il valore predefinito è 96.

### Esempi

Mostra come modificare l'immagine mentre Aspose.Words converte un documento in uno.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// modifica l'immagine mentre l'operazione di salvataggio la rende.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Possiamo regolare queste proprietà per cambiare la luminosità e il contrasto dell'immagine.
    // Entrambi sono su una scala 0-1 e sono a 0,5 per impostazione predefinita.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Possiamo regolare la risoluzione orizzontale e verticale con queste proprietà.
    // Ciò influenzerà le dimensioni dell'immagine.
    // Il valore predefinito per queste proprietà è 96.0, per una risoluzione di 96 dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Possiamo ridimensionare l'immagine usando questa proprietà. Il valore predefinito è 1,0, per un ridimensionamento del 100%.
    // Possiamo usare questa proprietà per negare qualsiasi cambiamento nelle dimensioni dell'immagine che potrebbe causare la modifica della risoluzione.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Guarda anche

* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../imagesaveoptions/)
* assemblea [Aspose.Words](../../../)


