---
title: FixedPageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words för .NET
description: Optimera JPEG-kvaliteten i dina HTML-dokument med FixedPageSaveOptions. Justera enkelt egenskapen JpegQuality för enastående bildskärpa.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Hämtar eller ställer in ett värde som avgör kvaliteten på JPEG-bilderna i HTML-dokumentet.

```csharp
public int JpegQuality { get; set; }
```

## Anmärkningar

Gäller endast när ett dokument innehåller JPEG-bilder.

Använd den här egenskapen för att hämta eller ställa in kvaliteten på bilderna i ett dokument när de sparas i fast sidformat. Värdet kan variera från 0 till 100 där 0 betyder sämst kvalitet men maximal komprimering och 100 betyder bästa kvalitet men minimal komprimering.

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

* class [FixedPageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
