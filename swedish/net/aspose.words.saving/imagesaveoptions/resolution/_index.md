---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words för .NET
description: Optimera dina bilder med ImageSaveOptions! Kontrollera horisontell och vertikal upplösning i DPI för fantastisk kvalitet och skärpa. Förbättra dina bilder idag!
type: docs
weight: 130
url: /sv/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

Ställer in både horisontell och vertikal upplösning för de genererade bilderna, i punkter per tum.

```csharp
public float Resolution { set; }
```

## Anmärkningar

Den här egenskapen har endast effekt när du sparar i rasterbildformat.

## Exempel

Visar hur man anger en upplösning när man renderar ett dokument till PNG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Ställ in egenskapen "Upplösning" till "72" för att rendera dokumentet i 72 dpi.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Ställ in egenskapen "Upplösning" till "300" för att rendera dokumentet i 300 dpi.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

### Se även

* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
