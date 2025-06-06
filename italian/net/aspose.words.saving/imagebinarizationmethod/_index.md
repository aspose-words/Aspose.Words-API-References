---
title: ImageBinarizationMethod Enum
linktitle: ImageBinarizationMethod
articleTitle: ImageBinarizationMethod
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.ImageBinarizationMethod per un'efficace binarizzazione delle immagini. Ottimizza l'elaborazione dei tuoi documenti con tecniche avanzate.
type: docs
weight: 5950
url: /it/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

Specifica il metodo utilizzato per binarizzare l'immagine.

```csharp
public enum ImageBinarizationMethod
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Threshold | `0` | Specifica il metodo di soglia. |
| FloydSteinbergDithering | `1` | Specifica il dithering utilizzando il metodo di diffusione degli errori Floyd-Steinberg. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
