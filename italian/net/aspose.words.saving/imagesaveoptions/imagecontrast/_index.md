---
title: ImageSaveOptions.ImageContrast
linktitle: ImageContrast
articleTitle: ImageContrast
second_title: Aspose.Words per .NET
description: Regola la proprietà ImageContrast in ImageSaveOptions per migliorare la nitidezza e la profondità delle tue immagini. Ottimizza le tue immagini senza sforzo!
type: docs
weight: 60
url: /it/net/aspose.words.saving/imagesaveoptions/imagecontrast/
---
## ImageSaveOptions.ImageContrast property

Ottiene o imposta il contrasto per le immagini generate.

```csharp
public float ImageContrast { get; set; }
```

## Osservazioni

Questa proprietà ha effetto solo quando si salva in formati di immagini raster.

Il valore predefinito è 0,5. Il valore deve essere compreso tra 0 e 1.

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
