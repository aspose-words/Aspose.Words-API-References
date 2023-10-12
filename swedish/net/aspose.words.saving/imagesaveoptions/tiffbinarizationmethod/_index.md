---
title: ImageSaveOptions.TiffBinarizationMethod
second_title: Aspose.Words för .NET API Referens
description: ImageSaveOptions fast egendom. Hämtar eller ställer in metod som används vid konvertering av bilder till 1 bpp format närSaveFormat ärTiff och TiffCompression är lika medCcitt3 ellerCcitt4 .
type: docs
weight: 170
url: /sv/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

Hämtar eller ställer in metod som används vid konvertering av bilder till 1 bpp format när[`SaveFormat`](../saveformat/) ärTiff och [`TiffCompression`](../tiffcompression/) är lika medCcitt3 ellerCcitt4 .

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

### Anmärkningar

Standardvärdet ärThreshold.

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


