---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Saving.ImagePixelFormat für optimale Pixelformate in Dokumentseitenbildern. Verbessern Sie die visuelle Darstellung Ihrer Dokumente mühelos!
type: docs
weight: 5970
url: /de/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Gibt das Pixelformat für die generierten Bilder der Dokumentseiten an.

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

Zeigt, wie Sie eine Bit-pro-Pixel-Rate auswählen, mit der ein Dokument in ein Bild gerendert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben an
// Wählen Sie ein Pixelformat für das Bild aus, das beim Speichern generiert wird.
// Verschiedene Bit-pro-Pixel-Raten wirken sich auf die Qualität und Dateigröße des generierten Bildes aus.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// Wir können ImageSaveOptions-Instanzen klonen.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
