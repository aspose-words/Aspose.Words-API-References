---
title: ImageWatermarkOptions Class
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.ImageWatermarkOptions. Anpassa dina bildvattenmärken enkelt med mångsidiga alternativ för förbättrad dokumentpresentation.
type: docs
weight: 3670
url: /sv/net/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class

Innehåller alternativ som kan anges när man lägger till ett vattenmärke med bilden.

För att lära dig mer, besök[Arbeta med vattenstämpel](https://docs.aspose.com/words/net/working-with-watermark/) dokumentationsartikel.

```csharp
public class ImageWatermarkOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ImageWatermarkOptions](imagewatermarkoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [IsWashout](../../aspose.words/imagewatermarkoptions/iswashout/) { get; set; } | Hämtar eller ställer in ett booleskt värde som ansvarar för vattenstämpelns uttvättningseffekt. Standardvärdet är`sann` . |
| [Scale](../../aspose.words/imagewatermarkoptions/scale/) { get; set; } | Hämtar eller ställer in skalfaktorn uttryckt som en bråkdel av bilden. Standardvärdet är 0 - auto. |

## Exempel

Visar hur man skapar en vattenstämpel från en bild i det lokala filsystemet.

```csharp
Document doc = new Document();

            // Ändra bildens vattenstämpels utseende med ett ImageWatermarkOptions-objekt,
            // skicka sedan den medan du skapar en vattenstämpel från en bildfil.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Vi har olika alternativ för att infoga bilder:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
