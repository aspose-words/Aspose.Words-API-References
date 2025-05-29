---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: Aspose.Words per .NET
description: Ottimizza le tue immagini con la soglia ImageSaveOptions per il dithering Floyd-Steinberg. Controlla l'errore di binarizzazione per risultati sorprendenti nell'elaborazione delle immagini.
type: docs
weight: 160
url: /it/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

Ottiene o imposta la soglia che determina il valore dell'errore di binarizzazione nel metodo Floyd-Steinberg. quando[`ImageBinarizationMethod`](../../imagebinarizationmethod/) ÈFloydSteinbergDithering .

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

## Osservazioni

Il valore predefinito è 128.

## Esempi

Mostra come impostare la soglia di errore di binarizzazione TIFF quando si utilizza il metodo Floyd-Steinberg per il rendering di un'immagine TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Quando salviamo il documento come TIFF, possiamo passare un oggetto SaveOptions a
// regola il dithering che Aspose.Words applicherà durante il rendering di questa immagine.
// Il valore predefinito della proprietà "ThresholdForFloydSteinbergDithering" è 128.
// I valori più alti tendono a produrre immagini più scure.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### Guarda anche

* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
