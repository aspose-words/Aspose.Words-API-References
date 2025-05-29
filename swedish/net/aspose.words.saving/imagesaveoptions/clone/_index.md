---
title: ImageSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words för .NET
description: Upptäck ImageSaveOptions Clone-metoden för att enkelt skapa en djup klon av dina objekt, vilket förbättrar din kodningseffektivitet och flexibilitet.
type: docs
weight: 210
url: /sv/net/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions.Clone method

Skapar en djup klon av detta objekt.

```csharp
public ImageSaveOptions Clone()
```

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

* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
