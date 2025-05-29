---
title: ImageSaveOptions.TiffBinarizationMethod
linktitle: TiffBinarizationMethod
articleTitle: TiffBinarizationMethod
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft TiffBinarizationMethod für ImageSaveOptions. Konvertieren Sie Bilder ganz einfach in das 1-bpp-Format mit CCITT3- oder CCITT4-Komprimierung.
type: docs
weight: 170
url: /de/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

Ruft die Methode ab oder legt sie fest, die beim Konvertieren von Bildern in das 1-bpp-Format verwendet wird , wenn[`SaveFormat`](../saveformat/) IstTiff und [`TiffCompression`](../tiffcompression/) ist gleichCcitt3 oderCcitt4 .

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

## Bemerkungen

Der Standardwert istThreshold.

## Beispiele

Zeigt, wie der Schwellenwert für den TIFF-Binarisierungsfehler festgelegt wird, wenn die Floyd-Steinberg-Methode zum Rendern eines TIFF-Bilds verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als TIFF speichern, können wir ein SaveOptions-Objekt übergeben an
// Passen Sie das Dithering an, das Aspose.Words beim Rendern dieses Bildes anwendet.
// Der Standardwert der Eigenschaft „ThresholdForFloydSteinbergDithering“ ist 128.
// Höhere Werte führen tendenziell zu dunkleren Bildern.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### Siehe auch

* enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
