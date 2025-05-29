---
title: ImageSaveOptions.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words för .NET
description: Upptäck ImageSize-egenskapen i ImageSaveOptions för att enkelt hantera och anpassa bilddimensioner i pixlar för optimala resultat.
type: docs
weight: 70
url: /sv/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Hämtar eller ställer in storleken på en genererad bild i pixlar.

```csharp
public Size ImageSize { get; set; }
```

## Anmärkningar

Den här egenskapen har endast effekt när du sparar i rasterbildformat.

Standardvärdet är (0 x 0), vilket innebär att storleken på den genererade bilden beräknas enligt bildens storlek i punkter, den angivna upplösningen och skalan.

## Exempel

Visar hur man renderar varje sida i ett dokument till en separat TIFF-bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Ställ in egenskapen "PageSet" till numret på den första sidan från
    // vilken dokumentet ska börja renderas från.
    options.PageSet = new PageSet(i);
    // Exportera sidan med 2325x5325 pixlar och 600 dpi.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### Se även

* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
