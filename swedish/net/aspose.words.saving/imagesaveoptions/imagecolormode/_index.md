---
title: ImageSaveOptions.ImageColorMode
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words för .NET
description: Upptäck ImageSaveOptions ImageColorMode-egenskapen för att enkelt anpassa och optimera färgläget för dina genererade bilder. Förbättra dina bilder idag!
type: docs
weight: 50
url: /sv/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

Hämtar eller ställer in färgläget för de genererade bilderna.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

## Anmärkningar

Den här egenskapen har endast effekt när du sparar i rasterbildformat.

Standardvärdet ärNone.

## Exempel

Visar hur man ställer in ett färgläge vid rendering av dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions-objekt till
// välj ett färgläge för bilden som sparandet kommer att generera.
// Om vi ställer in egenskapen "ImageColorMode" till "ImageColorMode.BlackAndWhite",
// sparoperationen kommer att tillämpa gråskalefärgreducering under rendering av dokumentet.
 // Om vi ställer in egenskapen "ImageColorMode" till "ImageColorMode.Grayscale",
// sparningsåtgärden kommer att återge dokumentet till en monokrom bild.
// Om vi ställer in egenskapen "ImageColorMode" till "None" kommer standardmetoden att användas vid sparning.
// och bevara alla dokumentets färger i utdatabilden.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### Se även

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
