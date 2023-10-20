---
title: ImageSaveOptions.TiffBinarizationMethod
linktitle: TiffBinarizationMethod
articleTitle: TiffBinarizationMethod
second_title: Aspose.Words per .NET
description: ImageSaveOptions TiffBinarizationMethod proprietà. Ottiene o imposta il metodo utilizzato durante la conversione delle immagini nel formato 1 bpp quandoSaveFormat ÈTiff e TiffCompression è uguale aCcitt3 OCcitt4  in C#.
type: docs
weight: 170
url: /it/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

Ottiene o imposta il metodo utilizzato durante la conversione delle immagini nel formato 1 bpp quando[`SaveFormat`](../saveformat/) ÈTiff e [`TiffCompression`](../tiffcompression/) è uguale aCcitt3 OCcitt4 .

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

## Osservazioni

Il valore predefinito èThreshold.

## Esempi

Mostra come impostare la soglia di errore di binarizzazione TIFF quando si utilizza il metodo Floyd-Steinberg per eseguire il rendering di un'immagine TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Quando salviamo il documento come TIFF, possiamo passare un oggetto SaveOptions a
// regola il dithering che Aspose.Words applicherà durante il rendering di questa immagine.
// Il valore predefinito della proprietà "ThresholdForFloydSteinbergDithering" è 128.
// Valori più alti tendono a produrre immagini più scure.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### Guarda anche

* enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
