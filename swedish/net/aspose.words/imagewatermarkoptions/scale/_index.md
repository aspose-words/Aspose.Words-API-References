---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words för .NET
description: ImageWatermarkOptions Scale fast egendom. Hämtar eller ställer in skalfaktorn uttryckt som en bråkdel av bilden. Standardvärdet är 0  auto i C#.
type: docs
weight: 30
url: /sv/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Hämtar eller ställer in skalfaktorn uttryckt som en bråkdel av bilden. Standardvärdet är 0 - auto.

```csharp
public double Scale { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kastar när argumentet var utanför intervallet för giltiga värden. |

## Anmärkningar

Giltiga värden sträcker sig från 0 till 65,5 inklusive.

Automatisk skala betyder att vattenstämpeln skalas till dess maxbredd och maxhöjd i förhållande till sidmarginalerna.

## Exempel

Visar hur man skapar en vattenstämpel från en bild i det lokala filsystemet.

```csharp
Document doc = new Document();

            // Ändra bildens vattenmärkes utseende med ett ImageWatermarkOptions-objekt,
            // skicka den sedan medan du skapar en vattenstämpel från en bildfil.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Se även

* class [ImageWatermarkOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
