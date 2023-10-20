---
title: FixedPageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words för .NET
description: FixedPageSaveOptions JpegQuality fast egendom. Hämtar eller ställer in ett värde som bestämmer kvaliteten på JPEGbilderna i HTMLdokumentet i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Hämtar eller ställer in ett värde som bestämmer kvaliteten på JPEG-bilderna i HTML-dokumentet.

```csharp
public int JpegQuality { get; set; }
```

## Anmärkningar

Har endast effekt när ett dokument innehåller JPEG-bilder.

Använd den här egenskapen för att få eller ställa in kvaliteten på bilderna i ett dokument när du sparar i fast sidformat. Värdet kan variera från 0 till 100 där 0 betyder sämsta kvalitet men maximal komprimering och 100 betyder bästa kvalitet men minsta komprimering.

Standardvärdet är 95.

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

* class [FixedPageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
