---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
second_title: Aspose.Words för .NET API Referens
description: ImageSaveOptions fast egendom. Hämtar eller ställer in tröskeln som bestämmer värdet för binariseringsfelet i FloydSteinbergmetoden. närImageBinarizationMethod ärFloydSteinbergDithering .
type: docs
weight: 160
url: /sv/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

Hämtar eller ställer in tröskeln som bestämmer värdet för binariseringsfelet i Floyd-Steinberg-metoden. när[`ImageBinarizationMethod`](../../imagebinarizationmethod/) ärFloydSteinbergDithering .

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

### Anmärkningar

Standardvärdet är 128.

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

* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../imagesaveoptions/)
* hopsättning [Aspose.Words](../../../)


