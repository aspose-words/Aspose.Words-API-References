---
title: ImageSaveOptions.ImageBrightness
linktitle: ImageBrightness
articleTitle: ImageBrightness
second_title: Aspose.Words för .NET
description: Justera ljusstyrkan på dina bilder enkelt med ImageSaveOptions-egenskapen. Förbättra dina bilder för fantastiska resultat!
type: docs
weight: 40
url: /sv/net/aspose.words.saving/imagesaveoptions/imagebrightness/
---
## ImageSaveOptions.ImageBrightness property

Hämtar eller ställer in ljusstyrkan för de genererade bilderna.

```csharp
public float ImageBrightness { get; set; }
```

## Anmärkningar

Den här egenskapen har endast effekt när du sparar i rasterbildformat.

Standardvärdet är 0,5. Värdet måste ligga i intervallet mellan 0 och 1.

## Exempel

Visar hur man redigerar bilden medan Aspose.Words konverterar ett dokument till ett.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions-objekt till
// redigera bilden medan sparoperationen renderar den.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Vi kan justera dessa egenskaper för att ändra bildens ljusstyrka och kontrast.
    // Båda är på en skala från 0 till 1 och är som standard på 0,5.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Vi kan justera horisontell och vertikal upplösning med dessa egenskaper.
    // Detta kommer att påverka bildens dimensioner.
    // Standardvärdet för dessa egenskaper är 96,0, för en upplösning på 96 dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Vi kan skala bilden med den här egenskapen. Standardvärdet är 1.0, för en skalning på 100%.
    // Vi kan använda den här egenskapen för att neutralisera eventuella förändringar i bildens dimensioner som en ändring av upplösningen skulle orsaka.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Se även

* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
