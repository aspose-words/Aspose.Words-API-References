---
title: ImageColorMode Enum
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.ImageColorMode-enum för att optimera dokumentsidor. Kontrollera färglägen för förbättrad visuell kvalitet i dina projekt.
type: docs
weight: 5960
url: /sv/net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

Anger färgläget för de genererade bilderna av dokumentsidor.

```csharp
public enum ImageColorMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Sidorna i dokumentet kommer att återges som färgbilder. |
| Grayscale | `1` | Sidorna i dokumentet kommer att återges som gråskalebilder. |
| BlackAndWhite | `2` | Sidorna i dokumentet kommer att återges som svartvita bilder. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
