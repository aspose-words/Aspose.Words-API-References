---
title: ImageSaveOptions
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck ImageSaveOptions-konstruktorn för att spara bilder i mångsidiga format som TIFF, PNG, BMP, JPEG, EMF, EPS, WebP och SVG. Optimera din bildhantering!
type: docs
weight: 10
url: /sv/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

Initierar en ny instans av den här klassen som kan användas för att spara renderade bilder i Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps , WebP ellerSvg format.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | SaveFormat | Kan vara Tiff ,Png ,Bmp , Jpeg ,Emf ,EpsWebP ellerSvg format. |

## Exempel

Visar hur man konfigurerar komprimering när man sparar ett dokument som JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Sätt egenskapen "JpegQuality" till "10" för att använda starkare komprimering vid rendering av dokumentet.
// Detta minskar dokumentets filstorlek, men bilden kommer att visa mer framträdande komprimeringsartefakter.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Sätt egenskapen "JpegQuality" till "100" för att använda svagare komprimering vid rendering av dokumentet.
// Detta kommer att förbättra bildens kvalitet till bekostnad av en ökad filstorlek.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
