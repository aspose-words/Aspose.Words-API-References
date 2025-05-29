---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PixelFormat i ImageSaveOptions för att enkelt anpassa pixelformatet för dina genererade bilder för optimal kvalitet och prestanda.
type: docs
weight: 120
url: /sv/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

Hämtar eller ställer in pixelformatet för de genererade bilderna.

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## Anmärkningar

Den här egenskapen har endast effekt när du sparar i rasterbildformat.

Standardvärdet ärFormat32BppArgb.

Pixelformatet för utdatabilden kan skilja sig från det inställda värdet på grund av GDI+:s arbete.

## Exempel

Visar hur man väljer en bit-per-pixel-hastighet för att rendera ett dokument till en bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions-objekt till
// välj ett pixelformat för bilden som sparandet kommer att generera.
// Olika bithastigheter per pixel påverkar kvaliteten och filstorleken på den genererade bilden.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// Vi kan klona ImageSaveOptions-instanser.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Se även

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
