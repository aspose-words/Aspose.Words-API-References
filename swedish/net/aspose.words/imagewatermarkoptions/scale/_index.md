---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Skala i ImageWatermarkOptions för att enkelt justera bildskalning för optimal vattenmärkning. Standardvärdet är 0 auto för sömlös integration.
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
| ArgumentOutOfRangeException | Kasta ett värde när argumentet låg utanför intervallet för giltiga värden. |

## Anmärkningar

Giltiga värden sträcker sig från 0 till 65,5.

Automatisk skalning innebär att vattenstämpeln skalas till sin maximala bredd och maximala höjd i förhållande till sidmarginalerna.

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

* class [ImageWatermarkOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
