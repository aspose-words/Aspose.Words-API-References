---
title: Enum ImagePixelFormat
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.ImagePixelFormat uppräkning. Anger pixelformatet för de genererade bilderna av dokumentsidor.
type: docs
weight: 4960
url: /sv/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Anger pixelformatet för de genererade bilderna av dokumentsidor.

```csharp
public enum ImagePixelFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 16 bitar per pixel, RGB. |
| Format16BppRgb565 | `1` | 16 bitar per pixel, RGB. |
| Format16BppArgb1555 | `2` | 16 bitar per pixel, ARGB. |
| Format24BppRgb | `3` | 24 bitar per pixel, RGB. |
| Format32BppRgb | `4` | 32 bitar per pixel, RGB. |
| Format32BppArgb | `5` | 32 bitar per pixel, ARGB. |
| Format32BppPArgb | `6` | 32 bitar per pixel, ARGB, förmultiplicerad alfa. |
| Format48BppRgb | `7` | 48 bitar per pixel, RGB. |
| Format64BppArgb | `8` | 64 bitar per pixel, ARGB. |
| Format64BppPArgb | `9` | 64 bitar per pixel, ARGB, förmultiplicerad alfa. |
| Format1bppIndexed | `10` | 1 bit per pixel, indexerad. |

### Exempel

Visar hur man väljer en bit-per-pixel-hastighet med vilken ett dokument ska renderas till en bild.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions-objekt till
            // välj ett pixelformat för bilden som sparas.
            // Olika bit per pixelhastigheter kommer att påverka kvaliteten och filstorleken på den genererade bilden.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.PixelFormat = imagePixelFormat;

            // Vi kan klona ImageSaveOptions-instanser.
            Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

            doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format32BppRgb:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(70000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                case ImagePixelFormat.Format32BppRgb:
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#endif
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


