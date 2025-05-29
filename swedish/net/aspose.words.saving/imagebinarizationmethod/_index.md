---
title: ImageBinarizationMethod Enum
linktitle: ImageBinarizationMethod
articleTitle: ImageBinarizationMethod
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.ImageBinarizationMethod-enum för effektiv bildbinarisering. Optimera din dokumentbehandling med avancerade tekniker.
type: docs
weight: 5950
url: /sv/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

Anger metoden som används för att binärisera bilden.

```csharp
public enum ImageBinarizationMethod
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Threshold | `0` | Anger tröskelmetod. |
| FloydSteinbergDithering | `1` | Anger dithering med Floyd-Steinbergs feldiffusionsmetod. |

## Exempel

Visar hur man ställer in tröskelvärdet för TIFF-binariseringsfel när Floyd-Steinberg-metoden används för att rendera en TIFF-bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// När vi sparar dokumentet som en TIFF kan vi skicka ett SaveOptions-objekt till
// justera ditheringen som Aspose.Words kommer att tillämpa när bilden renderas.
// Standardvärdet för egenskapen "ThresholdForFloydSteinbergDithering" är 128.
// Högre värden tenderar att ge mörkare bilder.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
