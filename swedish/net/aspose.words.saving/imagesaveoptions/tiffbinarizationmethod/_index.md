---
title: ImageSaveOptions.TiffBinarizationMethod
second_title: Aspose.Words för .NET API Referens
description: ImageSaveOptions fast egendom. Hämtar eller ställer in metod som används vid konvertering av bilder till 1 bpp format närSaveFormat är SaveFormat.Tiff and TiffCompression är lika med TiffCompression.Ccitt3 eller TiffCompression.Ccitt4.
type: docs
weight: 160
url: /sv/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

Hämtar eller ställer in metod som används vid konvertering av bilder till 1 bpp format när[`SaveFormat`](../saveformat/) är SaveFormat.Tiff and [`TiffCompression`](../tiffcompression/) är lika med TiffCompression.Ccitt3 eller TiffCompression.Ccitt4.

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

### Anmärkningar

Standardvärdet är ImageBinarizationMethod.Threshold.

### Exempel

Visar hur man ställer in TIFF-binariseringsfeltröskeln när man använder Floyd-Steinberg-metoden för att rendera en TIFF-bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// När vi sparar dokumentet som en TIFF kan vi skicka ett SaveOptions-objekt till
// justera vibreringen som Aspose.Words kommer att tillämpa när den här bilden renderas.
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

* enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../imagesaveoptions/)
* hopsättning [Aspose.Words](../../../)


