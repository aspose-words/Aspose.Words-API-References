---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.ImagePixelFormat opsomming. Gibt das Pixelformat für die generierten Bilder von Dokumentseiten an in C#.
type: docs
weight: 5220
url: /de/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Gibt das Pixelformat für die generierten Bilder von Dokumentseiten an.

```csharp
public enum ImagePixelFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 16 Bit pro Pixel, RGB. |
| Format16BppRgb565 | `1` | 16 Bit pro Pixel, RGB. |
| Format16BppArgb1555 | `2` | 16 Bit pro Pixel, ARGB. |
| Format24BppRgb | `3` | 24 Bit pro Pixel, RGB. |
| Format32BppRgb | `4` | 32 Bit pro Pixel, RGB. |
| Format32BppArgb | `5` | 32 Bit pro Pixel, ARGB. |
| Format32BppPArgb | `6` | 32 Bit pro Pixel, ARGB, vormultipliziertes Alpha. |
| Format48BppRgb | `7` | 48 Bit pro Pixel, RGB. |
| Format64BppArgb | `8` | 64 Bit pro Pixel, ARGB. |
| Format64BppPArgb | `9` | 64 Bit pro Pixel, ARGB, vormultipliziertes Alpha. |
| Format1bppIndexed | `10` | 1 Bit pro Pixel, indiziert. |

## Beispiele

Zeigt, wie Sie eine Bit-pro-Pixel-Rate auswählen, mit der ein Dokument in ein Bild gerendert werden soll.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt an übergeben
            // Wählen Sie ein Pixelformat für das Bild aus, das durch den Speichervorgang generiert wird.
            // Verschiedene Bit-pro-Pixel-Raten wirken sich auf die Qualität und Dateigröße des generierten Bildes aus.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.PixelFormat = imagePixelFormat;

            // Wir können ImageSaveOptions-Instanzen klonen.
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

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
