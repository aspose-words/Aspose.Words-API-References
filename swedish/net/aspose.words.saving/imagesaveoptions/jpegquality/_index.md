---
title: ImageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words för .NET
description: Justera egenskapen JpegQuality i ImageSaveOptions för att optimera JPEG-bildkvaliteten för fantastiska bilder och förbättrad prestanda. Perfekt för utvecklare!
type: docs
weight: 80
url: /sv/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

Hämtar eller ställer in ett värde som bestämmer kvaliteten på de genererade JPEG-bilderna.

```csharp
public int JpegQuality { get; set; }
```

## Anmärkningar

Gäller endast när man sparar som JPEG.

Använd den här egenskapen för att hämta eller ställa in kvaliteten på genererade bilder när de sparas i JPEG-format. Värdet kan variera från 0 till 100 där 0 betyder sämst kvalitet men maximal komprimering och 100 betyder bästa kvalitet men minimal komprimering.

Standardvärdet är 95.

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

* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
