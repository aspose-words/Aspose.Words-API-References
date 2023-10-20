---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: Aspose.Words för .NET
description: ImageWatermarkOptions IsWashout fast egendom. Hämtar eller ställer in ett booleskt värde som är ansvarigt för utspolningseffekten av vattenstämpeln. Standardvärdet ärSann  i C#.
type: docs
weight: 20
url: /sv/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Hämtar eller ställer in ett booleskt värde som är ansvarigt för utspolningseffekten av vattenstämpeln. Standardvärdet är`Sann` .

```csharp
public bool IsWashout { get; set; }
```

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
