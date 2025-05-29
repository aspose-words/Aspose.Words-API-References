---
title: ImageSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words för .NET
description: Upptäck ImageSaveOptions SaveFormat-egenskapen för att enkelt spara dokument i format som TIFF, PNG, JPEG med mera. Förbättra ditt arbetsflöde idag!
type: docs
weight: 140
url: /sv/net/aspose.words.saving/imagesaveoptions/saveformat/
---
## ImageSaveOptions.SaveFormat property

Anger formatet i vilket de renderade dokumentsidorna eller formerna sparas om det här objektet för sparade alternativ används. Kan vara ett raster Tiff ,Png ,Bmp , Jpeg eller vektorEmf ,Eps , WebP ,Svg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Anmärkningar

Antalet andra alternativ beror på det valda formatet.

Det är också möjligt att spara till SVG både via[`ImageSaveOptions`](../) och via[`SvgSaveOptions`](../../svgsaveoptions/).

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
