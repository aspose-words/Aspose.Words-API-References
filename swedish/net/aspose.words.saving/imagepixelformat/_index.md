---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.ImagePixelFormat-enum för optimala pixelformat i dokumentsidor. Förbättra dina dokumentbilder utan ansträngning!
type: docs
weight: 5970
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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
