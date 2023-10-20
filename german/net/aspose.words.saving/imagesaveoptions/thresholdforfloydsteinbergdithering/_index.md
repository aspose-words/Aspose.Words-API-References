---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: Aspose.Words für .NET
description: ImageSaveOptions ThresholdForFloydSteinbergDithering eigendom. Ruft den Schwellenwert ab oder legt diesen fest der den Wert des Binärisierungsfehlers in der FloydSteinbergMethode bestimmt. wannImageBinarizationMethod IstFloydSteinbergDithering  in C#.
type: docs
weight: 160
url: /de/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

Ruft den Schwellenwert ab oder legt diesen fest, der den Wert des Binärisierungsfehlers in der Floyd-Steinberg-Methode bestimmt. wann[`ImageBinarizationMethod`](../../imagebinarizationmethod/) IstFloydSteinbergDithering .

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

## Bemerkungen

Der Standardwert ist 128.

## Beispiele

Zeigt, wie der TIFF-Binarisierungsfehlerschwellenwert festgelegt wird, wenn die Floyd-Steinberg-Methode zum Rendern eines TIFF-Bilds verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als TIFF speichern, können wir ein SaveOptions-Objekt an übergeben
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

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
