---
title: ImageSaveOptions
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: Aspose.Words för .NET
description: ImageSaveOptions byggare. Initierar en ny instans av denna klass som kan användas för att spara renderade bilder i Tiff Png Bmp  Jpeg Emf Eps ellerSvg format i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

Initierar en ny instans av denna klass som kan användas för att spara renderade bilder i Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps ellerSvg format.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | SaveFormat | Kan vara Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps ellerSvg format. |

## Exempel

Visar hur du konfigurerar komprimering medan du sparar ett dokument som en JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Ställ in egenskapen "JpegQuality" till "10" för att använda starkare komprimering när du renderar dokumentet.
// Detta kommer att minska filstorleken på dokumentet, men bilden kommer att visa mer framträdande komprimeringsartefakter.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Ställ in egenskapen "JpegQuality" till "100" för att använda svagare komprimering när du renderar dokumentet.
// Detta kommer att förbättra kvaliteten på bilden till priset av en ökad filstorlek.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
